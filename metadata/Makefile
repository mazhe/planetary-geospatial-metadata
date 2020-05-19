SRC=$(shell find ./ -name "*.yml")
TRG=$(patsubst %.yml,%.xml,$(SRC))
 
default: $(SRC)
	make $(TRG)

%.xml: %.yml
	pygeometa generate-metadata --mcf=$<  --schema=iso19139 --output=$@
