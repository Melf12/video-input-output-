# Lyd output fra webcame (Nærkontakt fra 3 grad"
Filen som i skal kigge i er "SimpleVideoInputWithProcessing_100Inputs_lydoutput.pde"
Mit projekt:
I dette wekinator projekt, skulle vi integrere nogen lyde fra "nærkontakt af 3 grad" ind som et output. Jeg har brugt kamareret som input, hvor jeg så styrer hvilke beævgelser der skal give de forskellige lyde som outputs. Jeg har kommenteret de steder, hvor jeg har ændret koden i processing filen. Jeg har prøvet at lave nogen træningsdata til denne sketch med de 6 forskellige lydklasser, 1 værende intet støj. Herefter præøvde jeg at træne programmet til at spille de forskellige toner udfra håndbevægelser. Når jeg havde hånden åben, så stoppede lyden (klasse 1), når jeg kun havde løftet 1 finger, skulle første tone spille, 2 fingre anden tone osv. En så lille ændring var ret svær at få til at fungere, da der var en masse støj igennem små bevægelser og wekinator havde svært ved at gennemskue hvilken af klasserne den skulle spille. Det ville derfor her være relevant, at udnytte den metode, hvor wekinator først ændrer klassen efter den har konkluderet at fx 95% af bevægelsen havde ændret sig. Dette ville gøre det nemmere at udelukke noget af støjen. Det vil måske også gøre det nemmere hvis jeg brugte større bevægelser, måske bevæglse af hovedet. 




