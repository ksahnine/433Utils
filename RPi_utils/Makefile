prefix=/usr/local/bin

all: send codesend RFSniffer

send: RCSwitch.o send.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi
	
codesend: RCSwitch.o codesend.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi
	
RFSniffer: RCSwitch.o RFSniffer.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ -lwiringPi
	

clean:
	$(RM) *.o send codesend servo RFSniffer

install: all
	cp RFSniffer send codesend $(prefix)

uninstall:
	rm $(prefix)/RFSniffer
	rm $(prefix)/send
	rm $(prefix)/codesend
