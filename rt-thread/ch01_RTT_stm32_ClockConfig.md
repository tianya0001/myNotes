1. 修改时钟源频率

    修改  *stm32f4xx_hal_conf.h* 里 *HSE_VALUE* 为晶振频率（Hz）

2. 修改RCC配置

    对照STM32Cube生成的RCC配置函数修改 *drv_clk.c* 中 *void system_clock_config(int target_freq_mhz)* 函数


