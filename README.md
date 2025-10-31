System Resource Monitoring with Netdata

This repository documents the completion of Task 7, which involves installing and utilizing **Netdata**, a free, open-source, real-time performance monitoring tool, to visualize system and application metrics.

## Objective

To gain practical experience with lightweight, real-time monitoring by deploying Netdata and analyzing key performance metrics for a server environment.

## Tools Used

* **Netdata:** Real-time performance monitoring tool.
* **Docker:** Used to quickly deploy and isolate the Netdata service.
* **Operating System:** WSL2 (Windows Subsystem for Linux) / Linux / macOS (Based on the environment where Docker was run).

## Deployment Instructions (Mini-Guide)

Netdata was deployed using the official Docker image for ease and speed.

1.  **Ensure Docker is Running:** Verify that the Docker daemon is active on your host machine.
2.  **Run the Netdata Container:** Execute the following command in your terminal. This runs Netdata in the background (`-d`), names the container `netdata`, and maps the internal port 19999 to the host's port 19999.

       bash
    docker run -d \
      --name=netdata \
      -p 19999:19999 \
      netdata/netdata

3.  **Access the Dashboard:** Open your web browser and navigate to the local address:

    
    http://localhost:19999
    

## Key Monitoring Insights

Upon accessing the dashboard, the following system metrics were immediately visible and monitored in real-time:

* **CPU Utilization:** Tracking system, user, and iowait usage.
* **Memory and Swap:** Real-time analysis of RAM usage, swap activity, and kernel memory.
* **Disk I/O:** Monitoring read/write throughput and latency for storage devices.
* **Docker Container Metrics:** Real-time performance data for the Netdata container itself and other running containers (if applicable).
* **Alerts:** Exploration of pre-configured **smart alarms** that warn of anomalies or high resource consumption.

##  Deliverables

The primary deliverable for this task is a screenshot of the active Netdata dashboard.

### Screenshot of the Netdata Dashboard
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/6f50d284-74b6-4b37-b162-3e4c994a1e1d" />
you can view as per your needs by simply clicking add chart and taking required usage formula
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/3b4ee76c-f4c9-4b73-95ec-951f2b3a7e57" />

The image below showcases the real-time visualization of key system resources (CPU, Memory, Disk I/O) confirming successful deployment and resource monitoring
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/ea7ba923-4e1d-47c0-a7df-ab9c3d71265f" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/42880a46-498c-4bde-b165-cc3df9d144db" />

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/550f40f8-e931-4709-9bed-da81900b8468" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/7b49b0df-b34e-4f32-acb1-14b03f07e761" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/564d0b95-12bd-427e-9c77-c49405111667" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/90012db5-b6e2-42de-b2f9-6b2627d29219" />

screenshots showing the Netdata dashboard with charts updating in real-time (e.g., CPU, Memory, Disk I/O panels).

## Cleanup (Stopping Netdata)

To stop and remove the Netdata container after the task is complete:

open Git and type below for that
docker stop netdata
docker rm netdata
