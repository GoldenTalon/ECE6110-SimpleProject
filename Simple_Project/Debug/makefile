################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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
Simple_Project.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Simple_Project.list \

OBJCOPY_BIN += \
Simple_Project.bin \


# All Target
all: Simple_Project.elf secondary-outputs

# Tool invocations
Simple_Project.elf: $(OBJS) $(USER_OBJS) C:\Users\Paula\ECE6110-SimpleProject\Simple_Project\STM32L475VGTX_FLASH.ld
	arm-none-eabi-gcc -o "Simple_Project.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Paula\ECE6110-SimpleProject\Simple_Project\STM32L475VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Simple_Project.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Simple_Project.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Simple_Project.list"
	@echo 'Finished building: $@'
	@echo ' '

Simple_Project.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Simple_Project.bin"
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
