################################################################################
# MRS Version: 1.9.1
# 自动生成的文件。不要编辑！
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include zf_driver/subdir.mk
-include zf_device/subdir.mk
-include zf_components/subdir.mk
-include zf_common/subdir.mk
-include user_c/subdir.mk
-include sdk/Startup/subdir.mk
-include sdk/Peripheral/subdir.mk
-include sdk/Core/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_UPPER_DEPS)),)
-include $(ASM_UPPER_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_FLASH += \
E07_encoder_demo.hex \

SECONDARY_LIST += \
E07_encoder_demo.lst \

SECONDARY_SIZE += \
E07_encoder_demo.siz \


# 所有目标
all: E07_encoder_demo.elf secondary-outputs

# 工具调用
E07_encoder_demo.elf: $(OBJS) $(USER_OBJS)
	@	@	riscv-none-embed-gcc -march=rv32imafc -mabi=ilp32f -msmall-data-limit=8 -mno-save-restore -O0 -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -fno-common -pedantic -Wunused -Wuninitialized -Wall  -g -T "C:\Users\2017600918\OneDrive\桌面\CHV307_Library-master\CHV307_Library-master\Example\libraries\sdk\Ld\Link.ld" -nostartfiles -Xlinker --gc-sections -L"../" -L"C:\Users\2017600918\OneDrive\桌面\CHV307_Library-master\CHV307_Library-master\Example\libraries\zf_device" -Wl,-Map,"E07_encoder_demo.map" --specs=nano.specs -u _printf_float --specs=nosys.specs -Wl,--print-memory-usage -o "E07_encoder_demo.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@	@
E07_encoder_demo.hex: E07_encoder_demo.elf
	@	riscv-none-embed-objcopy -O ihex "E07_encoder_demo.elf"  "E07_encoder_demo.hex"
	@	@
E07_encoder_demo.lst: E07_encoder_demo.elf
	@	riscv-none-embed-objdump --source --all-headers --demangle --line-numbers --wide "E07_encoder_demo.elf" > "E07_encoder_demo.lst"
	@	@
E07_encoder_demo.siz: E07_encoder_demo.elf
	@	riscv-none-embed-size --format=berkeley "E07_encoder_demo.elf"
	@	@
# 其他目标
clean:
	-$(RM) $(ASM_UPPER_DEPS)$(OBJS)$(SECONDARY_FLASH)$(SECONDARY_LIST)$(SECONDARY_SIZE)$(ASM_DEPS)$(S_DEPS)$(S_UPPER_DEPS)$(C_DEPS) E07_encoder_demo.elf
	-@
secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_LIST) $(SECONDARY_SIZE)

.PHONY: all clean dependents

-include ../makefile.targets
