# Performance Configs

- Baseline config: `base_operan_georing_avhrr_forecasting_highres.yml`

Use the baseline as your base config. Override the necessary config arguments in other config files. Launch stacked:

```
../WeatherGenerator-private/hpc/launch-slurm.py \
    --nodes="${nodes}" --time=10:00 \
    --base-config performance/base_operan_georing_avhrr_forecasting_highres.yml \
    --config \
        "custom_config_stack_1.yml" \
        "custom_config_stack_2.yml" \
```
