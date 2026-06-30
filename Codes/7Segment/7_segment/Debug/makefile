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
7_segment.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
7_segment.list \

OBJCOPY_HEX += \
7_segment.hex \

OBJCOPY_BIN += \
7_segment.bin \


# All Target
all: 7_segment.elf secondary-outputs

# Tool invocations
7_segment.elf: $(OBJS) $(USER_OBJS) D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\7Segment\7_segment\STM32F100C6TX_FLASH.ld
	arm-none-eabi-gcc -o "7_segment.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Controllers\2026\STM32\STM32F103C6Tx\Codes\7Segment\7_segment\STM32F100C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="7_segment.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

7_segment.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "7_segment.list"
	@echo 'Finished building: $@'
	@echo ' '

7_segment.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "7_segment.hex"
	@echo 'Finished building: $@'
	@echo ' '

7_segment.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "7_segment.bin"
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
