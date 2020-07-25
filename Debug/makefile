################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include ThirdParty/FreeRTOS/org/Source/portable/MemMang/subdir.mk
-include ThirdParty/FreeRTOS/org/Source/portable/GCC/ARM_CM4F/subdir.mk
-include ThirdParty/FreeRTOS/org/Source/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
TemperatureLoggerRTOS.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TemperatureLoggerRTOS.list \

OBJCOPY_BIN += \
TemperatureLoggerRTOS.bin \


# All Target
all: TemperatureLoggerRTOS.elf secondary-outputs

# Tool invocations
TemperatureLoggerRTOS.elf: $(OBJS) $(USER_OBJS) /Users/huzaifaasif/STM32CubeIDE/workspace_1.0.2/TemperatureLoggerRTOS/STM32F401RETX_FLASH.ld
	arm-none-eabi-gcc -o "TemperatureLoggerRTOS.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/Users/huzaifaasif/STM32CubeIDE/workspace_1.0.2/TemperatureLoggerRTOS/STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TemperatureLoggerRTOS.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TemperatureLoggerRTOS.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TemperatureLoggerRTOS.list"
	@echo 'Finished building: $@'
	@echo ' '

TemperatureLoggerRTOS.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "TemperatureLoggerRTOS.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
