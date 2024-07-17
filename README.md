# WordPress with MySQL using Helm Subcharts:


This guide provides instructions for deploying a WordPress application with a MySQL database using Helm subcharts and exposing it through Ingress in a Kubernetes cluster.

## Overview
This Helm chart sets up a WordPress application with a MySQL database. It uses Helm subcharts to manage dependencies and utilizes Ingress for external access.

### Prerequisites 
Before you begin, ensure you have the following:

+ A Kubernetes cluster.

+ Helm 3.x installed. You can install Helm by following Helm's official documentation.

+ kubectl configured to interact with your Kubernetes cluster.

+ An Ingress controller installed ( NGINX Ingress Controller).
#### Chart Structure
The chart directory includes:

+ my-wordpress/ (main chart)

   + Chart.yaml (metadata for the WordPress chart)

    + values.yaml (default values for the WordPress chart)

     + templates/ (Kubernetes manifests)

  + charts/

    + mysql/ (subchart for MySQL)

      + Chart.yaml (metadata for the MySQL chart)

      + values.yaml (default values for the MySQL chart)

      + templates/ (Kubernetes manifests for MySQL)
