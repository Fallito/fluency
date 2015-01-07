TARGET=Textures.xbt
XBMCTEX=/build/buildd/kodi-14.0~git20141223.1015-final/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (i486-linux,arm)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /build/buildd/kodi-14.0~git20141223.1015-final/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

