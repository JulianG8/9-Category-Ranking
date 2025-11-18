# 9-Category-Ranking
This project aims to improve Yahoo’s standard 9-category fantasy basketball ranking system. Yahoo calculates category averages (points, rebounds, assists, blocks, steals, FT%, FG%, turnovers, and 3-pointers made), computes Z-scores for each category, and ranks players accordingly.

However, Z-scores assume normal distributions, and several fantasy basketball categories are not normally distributed. This leads to certain categories, namely those with skewed or heavy-tailed distributions being under- or over-represented in Yahoo's rankings. To address this, I applied a Yeo-Johnson transformation to normalize each category’s distribution before recalculating the Z-scores.

Additionally, for FG% and FT%, I modified Yahoo’s approach by incorporating both efficiency and shooting volume. Two players may have identical percentages but drastically different impacts depending on their attempt rates.
