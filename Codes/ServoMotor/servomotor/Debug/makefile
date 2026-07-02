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
servomotor.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
servomotor.list \

OBJCOPY_HEX += \
servomotor.hex \

OBJCOPY_BIN += \
servomotor.bin \


# All Target
all: servomotor.elf secondary-outputs

# Tool invocations
servomotor.elf: $(OBJS) $(USER_OBJS) D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\ServoMotor\servomotor\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "servomotor.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\ServoMotor\servomotor\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="servomotor.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

servomotor.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "servomotor.list"
	@echo 'Finished building: $@'
	@echo ' '

servomotor.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "servomotor.hex"
	@echo 'Finished building: $@'
	@echo ' '

servomotor.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "servomotor.bin"
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
