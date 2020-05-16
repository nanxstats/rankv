graph LR
  A[(VAERS <br> Data)] --> B(Quality <br> Control)
  B --> C(GPS Ranker)
  B --> D(PRR Ranker)
  B --> E(ROR Ranker)
  B --> F(BCPNN Ranker)
  C --> |EB Score| G(EBGM05)
  D --> |PRR Score| H(LB95)
  E --> |ROR Score| I(LB95)
  F --> |IC Score| J(Q0.025)
  G --> Y(Rank <br> Aggregator)
  H --> Y
  I --> Y
  J --> Y
  Y --> Z(Aggregated <br> Ranking <br> Score)

{
  "theme": "default",
  "fontFamily": "-apple-system, BlinkMacSystemFont"
}
