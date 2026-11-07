# Performance Configs

- Baseline config: `base_operan_georing_avhrr_forecasting_highres.yml`

Use the baseline as your base config. Override the necessary config arguments in other config files. Launch stacked:

```
../WeatherGenerator-private/hpc/launch-slurm.py \
    --nodes="${nodes}" --time=10:00 \
    --base-config ../weathergen-configs/performance/base_operan_georing_avhrr_forecasting_highres.yml \
    --config \
        "../weathergen-configs/performance/custom_config_stack_1.yml" \
        "../weathergen-configs/performance/custom_config_stack_2.yml" \
```
E.g.,

```
../WeatherGenerator-private/hpc/launch-slurm.py \
    --nodes=1 --time=10:00 \
    --base-config ../weathergen-configs/performance/base_operan_georing_avhrr_forecasting_highres.yml
```
or
```
../WeatherGenerator-private/hpc/launch-slurm.py \
    --nodes=1 --time=10:00 \
    --base-config ../weathergen-configs/performance/base_operan_georing_avhrr_forecasting_highres.yml \
    --config \
        "../weathergen-configs/performance/operan_1280.yml"
```