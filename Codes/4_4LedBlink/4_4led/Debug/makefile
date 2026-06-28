################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
4_4led.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
4_4led.list \

OBJCOPY_HEX += \
4_4led.hex \

OBJCOPY_BIN += \
4_4led.bin \


# All Target
all: 4_4led.elf secondary-outputs

# Tool invocations
4_4led.elf: $(OBJS) $(USER_OBJS) D:\Controllers\2026\STM32\stm32f106c6\Codes\4_4LedBlink\4_4led\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "4_4led.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Controllers\2026\STM32\stm32f106c6\Codes\4_4LedBlink\4_4led\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="4_4led.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

4_4led.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "4_4led.list"
	@echo 'Finished building: $@'
	@echo ' '

4_4led.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "4_4led.hex"
	@echo 'Finished building: $@'
	@echo ' '

4_4led.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "4_4led.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
