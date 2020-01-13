################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
manaco_ver0.0.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
manaco_ver0.0.list \


# All Target
all: manaco_ver0.0.elf secondary-outputs

# Tool invocations
manaco_ver0.0.elf: $(OBJS) $(USER_OBJS) C:\stm32\work\manaco_ver0.0\STM32F413CHUX_FLASH.ld
	arm-none-eabi-gcc -o "manaco_ver0.0.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\stm32\work\manaco_ver0.0\STM32F413CHUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="manaco_ver0.0.map" -Wl,--gc-sections -static -u _printf_float -u_scanf_float --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -u _scanf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

manaco_ver0.0.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "manaco_ver0.0.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
