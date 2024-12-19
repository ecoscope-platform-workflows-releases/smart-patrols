# SMART Patrols Workflow

This repository contains workflow scripts for processing SMART conservation data.

## Prerequisites

- [Pixi](https://pixi.sh/) package manager
- Python environment

## Installation

1. Install Pixi:
```bash
# Install Pixi using your system's package manager
# Documentation: https://pixi.sh/
```

## Configuration

### Environment Variables

Set up the following environment variables before running the workflow:

```bash
# SMART API Test Server Configuration
export ecoscope_workflows__connections__smart__test__server="https://smartapitest.smartconservationtools.org/smartapi/"
export ecoscope_workflows__connections__smart__test__username=<YOUR_USERNAME>
export ecoscope_workflows__connections__smart__test__password=<YOUR_PASSWORD>

# Output Configuration
export ECOSCOPE_WORKFLOWS_RESULTS=<OUTPUT_PATH>
```

Replace the following placeholders:
- `<YOUR_USERNAME>`: Your SMART API username
- `<YOUR_PASSWORD>`: Your SMART API password
- `<OUTPUT_PATH>`: Directory path where results will be stored

## Usage

1. Navigate to the workflow directory:
```bash
cd ecoscope-workflows-smart-patrols-workflow
```

2. Run the workflow:
```bash
pixi run python ecoscope_workflows_smart_patrols_workflow/cli.py \
    --config-file param.yaml \
    --execution-mode sequential \
    --no-mock-io
```

### Command Line Arguments

- `--config-file`: Path to the configuration YAML file
- `--execution-mode`: Set to `sequential` for sequential processing
- `--no-mock-io`: Use actual I/O operations (not mocked)

## Directory Structure

```
ecoscope-workflows-smart-patrols-workflow/
├── ecoscope_workflows_smart_patrols_workflow/
│   └── cli.py
└── param.yaml
```

## Support

For issues and questions, please create an issue in the repository's issue tracker.