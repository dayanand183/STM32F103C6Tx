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
switch.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
switch.list \

OBJCOPY_HEX += \
switch.hex \

OBJCOPY_BIN += \
switch.bin \


# All Target
all: switch.elf secondary-outputs

# Tool invocations
switch.elf: $(OBJS) $(USER_OBJS) D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\Switch\switch\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "switch.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\Switch\switch\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="switch.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

switch.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "switch.list"
	@echo 'Finished building: $@'
	@echo ' '

switch.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "switch.hex"
	@echo 'Finished building: $@'
	@echo ' '

switch.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "switch.bin"
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
