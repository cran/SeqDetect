CLEANEXTS = o a 

# Specify the target file and the install directory
OUTPUTFILE  = libSETT.a

# Default target
lib_ett: all
all: $(OUTPUTFILE)

# Build a from o's
$(OUTPUTFILE): ETT.o ETT_Decay.o ETT_Mappers.o ETT_Utils.o ETT_Wrapper.o
	$(AR) ru $@ $^
#	$(RANLIB) $@

# No rule to build john.o, paul.o, and johnpaul.o from .cpp 
# files is required; this is handled by make's database of
# implicit rules

clean: 
	for file in $(CLEANEXTS); do rm -f *.$$file; done
	
ETT.o: ETT.hpp ETT_Utils.hpp ETT_Mappers.hpp
ETT_Decay.o: ETT_Decay.hpp ETT_Utils.hpp
ETT_Mappers.o: ETT_Mappers.hpp ETT_Decay.hpp ETT_Utils.hpp
ETT_Utils.o: ETT_Utils.hpp
ETT_Wrapper.o: ETT_Wrapper.hpp ETT.hpp ETT_Utils.hpp
