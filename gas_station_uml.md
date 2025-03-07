# UML Activity Diagram for Buying Gas at a Gas Station

```mermaid
graph TD;
    Start -->|Arrive at Gas Station| SelectPayment;
    SelectPayment -->|Insert Card| AuthorizePayment;
    SelectPayment -->|Pay with Cash| PayCash;
    PayCash --> SelectGas;
    AuthorizePayment --> SelectGas;
    SelectGas -->|Choose Fuel Type| PumpGas;
    PumpGas -->|Finish Pumping| PrintReceipt;
    PrintReceipt -->|Print| End;
    PrintReceipt -->|No Receipt| End;
    End(("End Process"));

