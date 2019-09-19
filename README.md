# video-input-output-

Mit projekt:


Jeg har lavet til denne tk-dig aflevering, hvor jeg har brugt webcamet. 
Jeg har taget mit webcam, som på nuværende tidspunkt fungere som et input og gjort det til et output også.
Det fungere således, at når man åbner sin hånd, så vokser der en rektangel på skærmen. 
Samtidig, vil denne rektangel blive mindre, når man lukker hånden og herved kan man regulere størrelsen af denne rektangel med hånden.
For at gøre dette har jeg været inde i koden for webcamets input og derfra har jeg tilføjet en ny OscP5, med porten 12000. 
Jeg har derefter lavet en oscEvent, til min OscP5, som opsamler det input, webcamet får. Dette input altså oscmessage, har jeg taget og flyttet ind i en rektangels parametre (width og height)
Dvs. med mine inputs kan jeg nu træne wekinator, til at gøre min rektangel større og mindre altefter forskellige bevægelser. 
Jeg har så trænet programmet til at gøre width og height større, når hånden foran skærmen åbner sig ved at tage en masse test samples.
Det jeg har lavet kan sagtens gøres bedre ved at tilføje flere outputs end de 2 jeg har. Herfra kan man også ændre x og y værdien på rektanglen.

Typen af reggression jeg bruger i denne opgave er "Neural Network". 
Jeg bruger denne type regression fordi, da det er den mest præcise specielt til meget data, men det er nok ikke den mest optimale. 
Det tager meget lang tid at træne data'en og resultatet er nogenlunde det samme som lineær eller polonomiel.
Jeg har testet både lineær og polonomiel regressions modeller. Træningen af data er meget hurtigere og til det simple program jeg laver, vil det nok være tilstrækkelig præcist. 
et er dog ikke
