\[White-paper analysis]
🇬🇧
# Key points

## Self-custody

The protocol allows only the owner to ultimately move funds (no _trusted third parties_).

## Transparency / Non-obscurity

Respecting **Kerckhoff's Principle**.

## Devicelessness

No specific device required.

## Monetization

Incentivizing users non-inefficiently to ask for help while performing the protocol to generate demand for an ally (whom should require 0 trust).

## Coercion resistance

The protocol pursues the inability of an adversary to make the victim move funds or break the protocol against their will.

## No unintended negative incentives

The potential victim is not weak to blackmail by taking a device hostage and the adversary is not incentivized to kill the victim e.g. to pervent the victim from undoing a succesful coercion.


---
# Take-aways

## TTPs

**Trusted third parties** should, as usual, be avoided because they introduce costs and attack vectors.

## PBA vs KBA

**Possession-based authentication** introduces the problem of remote monitoring the key or device, again in terms of costs and attack vectors.  
If an object is required, that should be stored physically far from the owner for security reasons, which clashes with the need for availability for practical reasons. With KBA this problem translates to the security being determined by the protocol itself and the key being available at any time.

## ==Self-custody = resistance to coercion==

## Emergent obscurity

Being in an early stage, obscurity-based methods are incentivized by ignorance.

## Trade-off security - practicality

The trade-off resides in the balance between security and practicality, since a victim who's being coerced into performing the protocol against their will would have to be detained for an amount of time equal to the duration of the **Time-Lock Puzzle** ==(inversely proportional to the probability of success)==, which would otherwise be suspended by stopping to work on it. However, the duration of the **TLP** as measured from the most (computationally) powerful ally would dictate the minimum waiting time for transfering funds.


---
# Glossary

**Anti-obscurity**: Being helped by the adversary knowing how the protocol works (different from respecting the _Kerckhoff's Principle_, which contemplates the neutral case). E.g.: The knowledgeable ones would know trying is useless, the ignorants would become knowledgeable and be dissuaded while coercing.









---
\[Note operative]
🇮🇹
# Punti Chiave

## Autocustodia

Il protocollo concede esclusivamente al proprietario la scelta definitiva di muovere i fond (no _terze parti fidate_).

## Trasparenza / Non-oscurità

Rispettare il **Principio di Kerckhoff**.

## Indipendenza da dispositivi

Nessun dispositivo specifico richiesto.

## Monetizzazione

Inserire un meccanismo non-inefficientante di potenziamento del protocollo che richieda l'intervento di un alleato (al quale si può dare 0 fiducia)

## Resistenza alla coercizione

Il protocollo si pone come obiettivo l'impedire ad un avversario di costringere la vittima a spostare fondi o infrangere il protocollo contro la propria volontà.

## Assenza di incentivi negativi

La vittima non può essere ricattata prendendo ostaggio un dispositivo e l'avversario non dev'essere incentivato a uccidere la vittima e.g. per prevenire che quest'ultima annulli una coercizione che aveva avuto successo.


---
# Pillole

## Terze parti fidate

Come sempre, le **terze parti fidate** andrebbero evitate in quanto rappresentano ulteriori costi e vettori d'attacco.

## Autenticazione per possesso vs per conoscenza

L'autenticazione per possesso introduce il problema del monitoraggio a distanza di una chiave o un dispositivo, introducendo anch'essa costi e vettori d'attacco.
Se l'autenticazione richiede il possesso di un oggetto, quell'oggetto andrebbe conservato fisicamente lontano dall'utilizzatore per questioni di sicurezza, il che si scontrerebbe con la necessità di averlo a portata per questioni di praticità. Con l'autenticazione per conoscenza questo problema si traduce nell'attribuire la sicurezza al funzionamento del protocollo e la praticità nell'avere la chiave sempre a portata.

## ==Autocustodia = Resistenza alla coercizione==

## Oscurità emergente

Trovandoci in una fase precoce, i metodi basati sull'oscurità sono favoriti dall'ignoranza.

## Compromesso sicurezza - praticità

Il compromesso risiede nel bilanciare sicurezza e praticità, in quanto una vittima costretta ad eseguire il protocollo contro la propria volontà andrebbe trattenuta per un ammontare di tempo pari alla durata del **Time-Lock Puzzle** ==(inversamente proporzionale alla probabilità di successo)==, che altrimenti potrebbe essere interrotto smettendo di lavorarci. Tuttavia, la durata del TLP (misurata quando eseguita dall'alleato più potente) detterebbe il tempo minimo per poter effettuare un trasferimento di fondi.

---
# Glossario

**Anti-obscurity**: L'essere aiutati dal fatto che un avversario conosca il protocollo (diverso dal rispettare il _Principio di Kerckhoff_ che contempla lo scenario neutro). E.g.: Un avversario informato sa che tentare è inutile, un avversario non informato lo diventerà e sarà dissuaso durante la coercizione.