# QL
This is the Lab assignment for Software Construction. It is a DSL for questionnaires, called QL.

Here's a simple questionnaire in QL from the domain of tax filing:

```
form taxOfficeExample { 
  "Did you sell a house in 2010?"
    hasSoldHouse: boolean
  "Did you buy a house in 2010?"
    hasBoughtHouse: boolean
  "Did you enter a loan?"
    hasMaintLoan: boolean
    
  if (hasSoldHouse) {
    "What was the selling price?"
      sellingPrice: money
    "Private debts for the sold house:"
      privateDebt: money
    "Value residue:"
      valueResidue: money = 
        (sellingPrice - privateDebt)
  }
  
}
```

The assignment was graded with an 8.