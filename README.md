# Lyd output fra webcame (Nærkontakt fra 3 grad"
Filen som i skal kigge i er "SimpleVideoInputWithProcessing_100Inputs_lydoutput.pde"

Mit projekt:
I dette wekinator projekt, skulle vi integrere nogen lyde fra "nærkontakt af 3 grad" ind som et output. Jeg har brugt kamareret som input, hvor jeg så styrer hvilke beævgelser der skal give de forskellige lyde som outputs. Jeg har kommenteret de steder, hvor jeg har ændret koden i processing filen. Jeg har prøvet at lave nogen træningsdata til denne sketch med de 6 forskellige lydklasser, 1 værende intet støj. Herefter præøvde jeg at træne programmet til at spille de forskellige toner udfra håndbevægelser. Når jeg havde hånden åben, så stoppede lyden (klasse 1), når jeg kun havde løftet 1 finger, skulle første tone spille, 2 fingre anden tone osv. En så lille ændring var ret svær at få til at fungere, da der var en masse støj igennem små bevægelser og wekinator havde svært ved at gennemskue hvilken af klasserne den skulle spille. Det ville derfor her være relevant, at udnytte den metode, hvor wekinator først ændrer klassen efter den har konkluderet at fx 95% af bevægelsen havde ændret sig. Dette ville gøre det nemmere at udelukke noget af støjen. Det vil måske også gøre det nemmere hvis jeg brugte større bevægelser, måske bevæglse af hovedet. 

Herunder er det kode jeg har ændret, som også kan ses i processing dokumentet:

//Her henter jeg sinus kurven.
SinOsc sine;

//Her har jeg defineret et array "Lyde", som indeholder alle de frekvenser af tonerne jeg gerne vil afspille.
float[] lyde = {0,523.25, 783.99, 1046.50, 1174.66, 1318.51};

// Her laver jeg en Sinus funktion kalde "Sine". 
  sine = new SinOsc(this);
  //Funktion der spiller sinus kurven.
  sine.play();
 
  void oscEvent(OscMessage theOscMessage) {
  // synchronized(locking) {
  if (theOscMessage.checkAddrPattern("/wek/outputs")==true) {
    if (theOscMessage.checkTypetag("f")) { // looking for 1 control value
// Jeg har her lavet en integer, som jeg kalder "sinefreq". Den her integer definere jeg som min Oscmessage - 1, da jeg skal smide den ind i mit array og jeg skal bruge startværdien i arrayet "0".
      int sinefreq = (int) theOscMessage.get(0).floatValue() - 1;
      //Her ændrer jeg frekvensen med funktionen sine.freq, udfra mit array med forskellige frekvenser. I mit array indsætter jeg så min oscMessage, så hver gang jeg ændrer class vil den spille en ny lyd, da den går 1 værdi videre i arrayet.
      sine.freq(lyde[sinefreq]);
  
    } else {
      println("Error: unexpected OSC message received by Processing: ");
      theOscMessage.print();
    }
  }






