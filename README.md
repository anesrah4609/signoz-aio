# 🧰 signoz-aio - All-in-One Monitoring for Unraid

[![Download signoz-aio](https://img.shields.io/badge/Download%20signoz--aio-1f6feb?style=for-the-badge&logo=github&logoColor=white)](https://github.com/anesrah4609/signoz-aio)

## 📥 Download

Use this link to visit the download page:

[Download signoz-aio](https://github.com/anesrah4609/signoz-aio)

## 🖥️ What this is

signoz-aio is a single container for Unraid that brings several monitoring tools into one place.

It includes:

- SigNoz UI and API
- OpenTelemetry Collector
- ClickHouse
- ZooKeeper
- Optional local host monitoring
- Metrics, logs, Docker stats, and OTLP intake

This setup helps you see what your server is doing without installing each part by hand.

## ✅ What you need

Before you start, make sure you have:

- A Windows computer to open the GitHub page and prepare the setup
- An Unraid server with Docker turned on
- Enough free disk space for logs and metrics
- A stable network connection
- Access to your Unraid web page

If you plan to track more than one app or container, give the system more CPU and memory.

## 🚀 Getting Started

Follow these steps in order:

1. Open the download page: [signoz-aio](https://github.com/anesrah4609/signoz-aio)
2. Read the page for the current install file or Unraid container info
3. Download the package or copy the needed container details
4. Open your Unraid web interface
5. Go to the Docker tab
6. Add a new container or install from the app source you use on Unraid
7. Paste the container settings from the project page
8. Apply the changes and wait for the container to start

If the page includes a release file, use that file. If it shows a general project page, use the install data on that page.

## ⚙️ Setup on Unraid

After the container is added, check these common settings:

- **Web UI ports**: keep the default ports unless the project page says otherwise
- **Storage paths**: map the app data to a disk path that stays on your server
- **Memory**: set enough RAM for ClickHouse and the SigNoz stack
- **Network mode**: use the mode listed in the project instructions
- **Environment values**: enter any values shown on the GitHub page

If you want local host monitoring, turn on the built-in host checks in the container options. This can collect:

- CPU use
- Memory use
- Disk use
- Docker container stats
- Logs from the host
- OTLP data from other apps

## 🧭 First Run

When the container starts for the first time:

1. Wait until all parts finish loading
2. Open the SigNoz web page from the container or Unraid app page
3. Check that the UI opens in your browser
4. Let it run for a few minutes so it can begin collecting data
5. Open a test app or container that sends metrics or logs if you have one

The first start can take longer because ClickHouse and ZooKeeper need time to get ready.

## 📊 What you can monitor

With signoz-aio, you can keep an eye on:

- Server health
- App logs
- Container CPU and memory use
- Request traces
- Metrics from apps that use OTLP
- Basic host activity
- Storage use over time

This makes it easier to spot slow apps, full disks, or services that stop working.

## 🔌 Sending data to SigNoz

You can point apps and tools at the OTLP endpoint in this container.

Common data types include:

- Traces
- Metrics
- Logs

If your app already supports OpenTelemetry, set its OTLP address to the host and port shown in the project settings. Then restart the app and check the SigNoz UI for incoming data.

## 🧩 Troubleshooting

If the app does not start:

- Check the Docker log in Unraid
- Make sure the data path exists and has write access
- Confirm that the port is free
- Check that enough RAM is available
- Restart the container and wait a few minutes

If the UI does not open:

- Verify the web port in the Unraid container settings
- Try another browser tab
- Make sure the container is still running

If data does not appear:

- Check the OTLP address in the sending app
- Confirm that host monitoring is turned on if you want local data
- Wait a few minutes for the first data points

## 🗂️ Helpful project topics

This project fits common home lab and self-hosted use cases:

- observability
- monitoring
- metrics
- logging
- telemetry
- tracking
- docker
- unraid
- self-hosted
- opentelemetry
- clickhouse
- zookeeper

## 🔄 Typical use case

A common setup is:

- One Unraid server runs signoz-aio
- One or more containers send logs and metrics
- You open the SigNoz UI in a browser
- You check system health in one place
- You use the data to find issues faster

## 🧱 Basic storage layout

A simple storage setup can include:

- One app data folder for SigNoz
- One database folder for ClickHouse
- One config folder for collector settings
- One log folder for container logs

Keep these folders on persistent storage so your data stays after a restart

## 🌐 Browser access

After install, you usually use a web browser to open the SigNoz UI.

If you are on Windows:

1. Open your browser
2. Type the address shown in Unraid
3. Sign in if the app asks for it
4. Use the dashboard to view metrics and logs

If the page does not load, recheck the port and container status in Unraid

## 📦 Files and services inside the stack

This container bundles several services together:

- SigNoz UI/API for viewing data
- OpenTelemetry Collector for data intake
- ClickHouse for storage
- ZooKeeper for coordination
- Host monitoring tools for local system data

That means fewer separate installs and fewer moving parts to manage

## 🛠️ Common checks after install

After setup, check these items:

- The container shows as running
- The web UI opens
- Data folders exist on disk
- Logs are being written
- OTLP data shows up from at least one source
- CPU and memory use stay within your limits

## 📚 Project link

Use the main project page here:

[https://github.com/anesrah4609/signoz-aio](https://github.com/anesrah4609/signoz-aio)