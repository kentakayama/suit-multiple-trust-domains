EXAMPLES = \
	example0_dependent.suit example1_process.suit example2_integrated.suit \
	example0_dependent.hex example1_process.hex example2_integrated.hex

.PHONY: all
all: $(EXAMPLES)

%.suit: %.diag
	diag2cbor.rb < $< > $@

%.hex: %.suit
	xxd -p -u $< > $@

.PHONY: clean
clean:
	$(RM) *.suit *.hex
