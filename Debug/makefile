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
FSR_test1.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
FSR_test1.list \

OBJCOPY_BIN += \
FSR_test1.bin \


# All Target
all: FSR_test1.elf secondary-outputs

# Tool invocations
FSR_test1.elf: $(OBJS) $(USER_OBJS) /home/blackbirdx/STM32CubeIDE/workspace_1.3.0/FSR_test1/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "FSR_test1.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/blackbirdx/STM32CubeIDE/workspace_1.3.0/FSR_test1/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="FSR_test1.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

FSR_test1.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "FSR_test1.list"
	@echo 'Finished building: $@'
	@echo ' '

FSR_test1.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "FSR_test1.bin"
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
