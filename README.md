# ZorbaEncrypt
Simple Encryption Algorithm


### bozza logica e funzionamento

#### prime operazioni e funzione

Si prende la sequenza di bit la si divide in 2, una parte del messaggio entrerà dentro la funzione che va ad operare alcune operazioni. Inizialmente si inverte interamente la porzione della sequenza e poi la si combina con la sottochiave, sostituendo il primo bit del messaggio con il secondo della chiave e così via ( ```msg[x] = s_key[x+1] ``` ).

#### XOR e ciclo

La funzione ritorna la sequenza alterata e la combina in un ```np.XOR_bitwise(msg, key)```, ovvero uno XOR bit a bit. Tutte le operazioni vengono eseguite 5 volte sulla parte di messaggio non alterata e poi alla fine verranno unite.
