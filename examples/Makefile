CC=cc
CXX=c++
CFLAGS = -O3 -Wall -pedantic -ansi -Wtraditional -I..
CXXFLAGS = -O3 -Wall -W -ansi -I..
LIBS = -lsequence -L/usr/local/lib
REGEX= -lboost_regex
all: codons.o gestimator.o msstats.o int_handler.o getopt.o getopt1.o baseComp.o valid_dna.o FastaExplicit.o translateTest.o slidingWindow.o slidingWindow2.o PolyTableIterators.o correlations.o critical_values.o ufs.o ms--.o msbeta.o freerec.o bottleneck.o fragments.o
	$(CXX) $(CXXFLAGS) $(LIBS)  ufs.o -o ufs
	$(CXX) $(CXXFLAGS) $(LIBS)  codons.o -o codons
	$(CXX) $(CXXFLAGS) $(LIBS)  msstats.o -o msstats
	$(CXX) $(CXXFLAGS) $(LIBS)  gestimator.o int_handler.o getopt.o getopt1.o -o gestimator
	$(CXX) $(CXXFLAGS) $(LIBS)  baseComp.o -o baseComp
	$(CXX) $(CXXFLAGS) $(LIBS)  FastaExplicit.o -o FastaExplicit
	$(CXX) $(CXXFLAGS) $(LIBS)  translateTest.o -o translateTest
	$(CXX) $(CXXFLAGS) $(LIBS)  slidingWindow.o -o slidingWindow
	$(CXX) $(CXXFLAGS) $(LIBS)  slidingWindow2.o -o slidingWindow2
	$(CXX) $(CXXFLAGS) $(LIBS)  PolyTableIterators.o -o PolyTableIterators
	$(CXX) $(CXXFLAGS) correlations.o -o correlations -lgsl -lgslcblas
	$(CXX) $(CXXFLAGS) critical_values.o -o critical_values
	$(CXX) $(CXXFLAGS) $(LIBS) -lgsl -lgslcblas ms--.o -o ms-- 
	$(CXX) $(CXXFLAGS) $(LIBS) -lgsl -lgslcblas msbeta.o -o msbeta 
	$(CXX) $(CXXFLAGS) $(LIBS) -lgsl -lgslcblas freerec.o -o freerec
	$(CXX) $(CXXFLAGS) $(LIBS) -lgsl -lgslcblas bottleneck.o -o bottleneck
	$(CXX) $(CXXFLAGS) $(LIBS) -lgsl -lgslcblas fragments.o -o fragments
	$(CXX) $(CXXFLAGS) $(LIBS)  $(REGEX) valid_dna.o -o valid_dna

clean:
	rm -f *.o codons msstats gestimator baseComp valid_dna FastaExplicit translateTest \
	slidingWindow slidingWindow2 PolyTableIterators  correlations \
	critical_values ufs ms-- msbeta freerec bottleneck fragments

