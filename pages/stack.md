# Stack

*So what did I build exactly?*

I spread out the services on different machines. Communication within one operating system is often trivial, so sending the data over different protocols seemed interesting.

The machines are also locally disperse. The thought was to have some network latency effects to see how those would influence the architecture of this system.

Here I hope to give you an insight, what I used to build my own personal data pipeline. I detail which software and (virtual) hardware I use to extract, store, analyse and display data.

## APIs and ETLs

This server is a e2-medium VM instance hosted on **Google Cloud**, located in Singapore. It runs ETL scripts with the **Apache Airflow**. The meta data airflow creates is stored locally in a **PostgreSQL** database. Its purpose is to constantly query APIs for live data and continuously store it away.

![Screenshot of the Airflow Interface showing the average execution time of DAGS](/static/instance-0-airflow-screenshot.webp)

It currently clocks in at about 30% average CPU load. So it seems like I need to find a few more things for it to do.

## AWS Database

The Data is sent directly to a db.t2.micro instance on **AWS RDB**. This one also runs **PostgreSQL**. Sometimes I'm not really sure where it is located exactly, but the time it takes for data to arrive there indicates, it's somewhere in the western hemisphere. It's really easy to loose your machines on AWS. You can still ping them but can't find them in the interface ...

![Screenshot of the AWS RDB Dashboard](/static/aws-rdb-screenshot.webp)

This one could also take a bit more pressure by the looks of it.

## Analysis

The Analysis of data is developed on on my local machine, mainly with **Jupyter Notebooks**, since a bunch of RAM and CPU cycles do come in handy when exploring data sets. I also utilise **Tableau**. It is it's own little beast but it ties in really well with all kinds of sources. It does lack a certain precision or clarity, that I appreciate when I'm manipulating **Pandas DataFrames** but I can absolutely see its appeal.  


## instance-1.net

Instance-1 is run on a f1-micro instance on **Google Cloud**, and I'm really fond of it. It does take a little effort and thought to make it run a web server with just a few hundred Megabytes of RAM. But it's much more fun driving a slow car fast than the other way round. (It does reminds me of optimising 640KiB to be able to run Monkey Island.)

![Screenshot of $ free -h on instance-1.net terminal](/static/instance-1-free-screenshot.webp)

Just like instance-0 it runs **Ubuntu**. I originally started my Linux journey on **Debian Sarge**, however I've gotten used to the way Ubuntu - it normally just automatically recognises any hardware I throw at it, so it's got that going for it.

This web site runs on **Flask**, you can have a look into the source code in [its GitHub repository](https://github.com/alexladda/instance-blog). I tried as much as I could to [separate my content](https://github.com/alexladda/instance-content) from the logic of the blog itself, so you can go ahead and just use it for your blog, if you feel like it.
