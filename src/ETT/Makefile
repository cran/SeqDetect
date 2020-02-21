CLEANEXTS = o a 
OUTPUTFILE  = libSETT.a

lib_ett: all
all: $(OUTPUTFILE)

$(OUTPUTFILE): ETT.o ETT_Decay.o ETT_Mappers.o ETT_Utils.o ETT_Wrapper.o
	$(AR) ru $@ $^

clean: 
	for file in $(CLEANEXTS); do rm -f *.$$file; done
	
ETT.o: ETT.hpp ETT_Utils.hpp ETT_Mappers.hpp
ETT_Decay.o: ETT_Decay.hpp ETT_Utils.hpp
ETT_Mappers.o: ETT_Mappers.hpp ETT_Decay.hpp ETT_Utils.hpp
ETT_Utils.o: ETT_Utils.hpp
ETT_Wrapper.o: ETT_Wrapper.hpp ETT.hpp ETT_Utils.hpp
