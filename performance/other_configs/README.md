# Preprint configs for the post-hackathon benchmarks

Copied unchanged from ecmwf/WeatherGenerator `f896fa3669f3b2edf1f2f08a2bd46320785d97e8`
(branch `shmh40/dev/safe-seminar-develop-ssl-diffusion-v1`), stages 1 and 2 of
`config/gjl_repro_forecast_n320_iasi_channels_pipeline.yml`. The only change is
`streams_directory`, which points to the copied stream folders in `streams/`.

| File | Use |
|---|---|
| `config_gjl6a0kb_reproduction_n320_iasi_channels.yml` | config 1, Preprint-Pretraining: `--base-config` |
| `config_gjl_repro_finetune_forecast_n320_iasi_channels.yml` | config 2, Preprint-Forecasting, from scratch: `--base-config` the file above plus `--config` this overlay |

Streams: `streams/gjl6a0kb_reproduction_n320_new_channels_iasi_channels/` (config 1) and
`streams/gjl6a0kb_reproduction_n320_new_channels_forecast_iasi_channels/` (config 2).

The relative `streams_directory` works because the launcher (WeatherGenerator-private
`launch-slurm.py`) copies this repository next to the WeatherGenerator copy of the job. The
benchmarks are described in weathergenerator-experiments,
`experiments/performance/2026-11-post-hackathon-benchmarks/other_configs/`.
