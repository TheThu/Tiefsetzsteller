################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F3xx_HAL_Driver/Src/subdir.mk
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
Tiefsetzsteller.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Tiefsetzsteller.list \

OBJCOPY_BIN += \
Tiefsetzsteller.bin \


# All Target
all: Tiefsetzsteller.elf secondary-outputs

# Tool invocations
Tiefsetzsteller.elf: $(OBJS) $(USER_OBJS) /Users/T2/Desktop/Embedded_C/T2_Projekte/target/Tiefsetzsteller/STM32F303K8TX_FLASH.ld
	arm-none-eabi-gcc -o "Tiefsetzsteller.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/Users/T2/Desktop/Embedded_C/T2_Projekte/target/Tiefsetzsteller/STM32F303K8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Tiefsetzsteller.map" -Wl,--gc-sections -static -specs=rdimon.specs -lc -lrdimon --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Tiefsetzsteller.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Tiefsetzsteller.list"
	@echo 'Finished building: $@'
	@echo ' '

Tiefsetzsteller.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Tiefsetzsteller.bin"
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
