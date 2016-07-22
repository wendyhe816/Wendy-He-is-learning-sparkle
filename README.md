# Wendy-He-is-learning-sparkle
Making open data social and meaningful with Semantic Web

PREFIX WH: <http://data.world/wendyhe/new-york-city-open-budget/Expense%20Budget.csv/Expense%20Budget#> 
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT (SUM(xsd:integer(?Adopted_Budget_Amount)) / 2 AS ?Total_budget)

WHERE 
{
    ?person WH:Budget_Code_Number "0020" .
    ?person WH:Adopted_Budget_Amount ?Adopted_Budget_Amount .
}
