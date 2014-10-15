    def piastrequadrate(b,h,i,c):
        if b==h:
            return i+1,c+1
        if b>h:
            return piastrequadrate(b-h,h,i+1,c+h)
        else:
            return piastrequadrate(b,h-b,i+1,c+b)
    def piastrellamento(b,h):
        return piastrequadrate(b,h,0,0)
    
    
Il piastrellamento può essere fatto solo con piastrelle quadrate e ho notato che le piastrelle costano di meno quando
sono più grandi. 

Cercherò quindi di piastrellarlo con piastrelle più grandi possibili ( ovviamente quadrate).

La funzione piastrequadrate(..) serve appunto per prendere l'altezza e la base e fare la prima piastrella più grande possibile.

Es: se hai un pavimento (muro) di h=8 e b=5 piastrequadrate(b,h,0,0) (i due zeri sono dei contatori che si vanno sommando quindi
devono iniziare da 0) creerà la piastrella iniziale di grandezze 5x5 poi 3x3 , 2x2 , 1x1 e infine l'ultima 1x1.

La funzione piastrequadrate inoltre avendo i due contatori "i" e "c" conta anche i passi con "i" e il costo (che equivale al lato
del quadrato della piastrella) del piastrellamento.

L'output del programma indicherà ( numero di passi fatti ricorsivamente, costo totale del piastrellamento ) la virgola sul return della terza riga tra "i+1" e "c+1" serve per fare stampare i due valori nello stesso return (+1 perchè non piastrequadrate non conta l'ultimo passaggio/ultima piastrella da 1x1 -> stessa cosa per c+1 non viene contato il costo dell'ultima piastrella {1} .

Spero di esservi stato utile!
