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
dcmotor.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
dcmotor.list \

OBJCOPY_HEX += \
dcmotor.hex \

OBJCOPY_BIN += \
dcmotor.bin \


# All Target
all: dcmotor.elf secondary-outputs

# Tool invocations
dcmotor.elf: $(OBJS) $(USER_OBJS) D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\DCMotor\dcmotor\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "dcmotor.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\DCMotor\dcmotor\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="dcmotor.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

dcmotor.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "dcmotor.list"
	@echo 'Finished building: $@'
	@echo ' '

dcmotor.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "dcmotor.hex"
	@echo 'Finished building: $@'
	@echo ' '

dcmotor.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "dcmotor.bin"
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
