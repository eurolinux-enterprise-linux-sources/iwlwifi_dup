fw =  iwlwifi-7260-13.ucode iwlwifi-7265-13.ucode iwlwifi-7265D-13.ucode

firmware: $(fw)

install: $(fw)
	for f in $+; do \
		install -m 644 -D $$f $(INSTALL_PATH)/lib/firmware/$(INSTALL_DIR)/$$f; \
	done

%:: %.ihex
	objcopy -Iihex -Obinary $< $@

%.fw: %.HEX ihex2fw
	./ihex2fw $< $@

%.fw: %.H16 ihex2fw
	./ihex2fw -w $< $@

ihex2fw: ihex2fw.c
	gcc -o $@ $<
