# mobile-metrics-dashboard

Interactive dashboard for representable [mobile metrics](https://github.com/matsoftware/mobile-metrics) data, built with **Python 3.7.1** using **Dash** and **Plotly Express**.

## Pre-requisites

1. Install all the needed dependencies by running `./install.sh` from the `dashboard` folder. 

2. Create a `.env` file in the `dashboard` of the repo with the local server settings, including the `API_SECRET` that you set in the backend before:
    ```bash
    BACKEND_HOST=http://localhost
    BACKEND_PORT=3000
    API_SECRET=my-custom-token
    DEBUG=true
    ```

3. Run the server with `./run.sh`

## Configuration

The dashboard can be configured by editing the `config.yml` file:

```yaml
title: 'Mobile Metrics Dashboard'
repo_name: 'Main repository'
footer_text: 'Ⓒ 2020 <author>'
render_metrics:
    app_size:
        download_size_trend: true
        install_size_trend: true
    code_metrics:
        total_loc: true
        main_repo_loc: true
        n_of_dependencies: true
```

The `render_metrics` section will let you configure which chart you want to display.