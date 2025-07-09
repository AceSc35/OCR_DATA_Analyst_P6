# OCR_Data_Analyst_P6


<h2>📊 Analyse des ventes clients – Data Science avec Python</h2>

<h3>⚙️ Prérequis</h3>
<p>Pour exécuter ce projet dans un environnement Python (Jupyter Notebook), les bibliothèques suivantes sont nécessaires :</p>
<ul>
  <li><code>plotly</code> : <code>pip install plotly</code></li>
  <li><code>statsmodels</code> : <code>pip install statsmodels</code></li>
</ul>

<h3>🎯 Objectif</h3>
<p>
Ce projet a pour objectif de réaliser une analyse exploratoire et statistique des ventes d’une librairie entre <strong>mars 2021 et février 2023</strong>. L’étude porte sur l’évolution du chiffre d’affaires, les performances produits, ainsi que le comportement d’achat des clients selon leurs caractéristiques.
</p>

<h3>📦 Données disponibles</h3>
<ul>
  <li><strong>Ventes :</strong> date, canal de vente, montant, catégorie de produit, référence</li>
  <li><strong>Clients :</strong> genre, âge, type de canal (physique / en ligne)</li>
</ul>

<h3>📈 Méthodologie</h3>
<ol>
  <li><strong>Analyse temporelle du CA</strong><br>
    - Évolution mensuelle / annuelle<br>
    - Moyennes mobiles pour dégager la tendance</li>
    

  <li><strong>Analyse produit</strong><br>
    - Identification des top/flop produits par CA et volume<br>
    - Répartition par catégories</li>
    

  <li><strong>Analyse client</strong><br>
    - Distribution du CA par client (loi de Pareto, courbe de Lorenz)<br>
    - Comparaison entre clients en ligne vs en librairie</li>

  <li><strong>Analyse statistique – Tests de corrélation</strong><br>
    <p>Plusieurs tests statistiques ont été utilisés pour mesurer la dépendance entre variables démographiques et comportementales :</p>
    <table border="1" cellpadding="5" cellspacing="0">
      <thead>
        <tr>
          <th>Hypothèse</th>
          <th>Variables concernées</th>
          <th>Test appliqué</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Genre influence la catégorie de livres achetés</td>
          <td>Genre (catégorielle) / Catégorie</td>
          <td>Test du Khi² (Chi-squared test)</td>
        </tr>
        <tr>
          <td>L’âge a un effet sur le panier moyen</td>
          <td>Âge (quantitatif) / Panier moyen</td>
          <td>Corrélation de Spearman</td>
        </tr>
        <tr>
          <td>L’âge influence la fréquence d’achat</td>
          <td>Âge regroupé / Nb d’achats</td>
          <td>ANOVA</td>
        </tr>
        <tr>
          <td>L’âge influence le montant total dépensé</td>
          <td>Âge (quantitatif) / CA total</td>
          <td>Corrélation de Spearman</td>
        </tr>
        <tr>
          <td>Les distributions sont normales pour valider les tests</td>
          <td>Données continues (montants, fréquences)</td>
          <td>Test de Shapiro-Wilk</td>
        </tr>
      </tbody>
    </table>
  </li>
</ol>

<h3>📊 Résultats principaux</h3>
<ul>
  <li>Le CA progresse régulièrement entre 2021 et 2022, malgré des baisses saisonnières.</li>
  <li>Les meilleures références concentrent une part importante du chiffre d’affaires.</li>
  <li>Les clients en ligne achètent plus fréquemment mais avec des paniers moyens plus faibles que les clients physiques.</li>
  <li>Aucune corrélation significative n’a été trouvée entre le genre et la catégorie de livres achetée.</li>
</ul>

<h3>🛠️ Stack technique</h3>
<ul>
  <li><strong>Python :</strong> pandas, numpy, matplotlib, seaborn, plotly</li>
  <li><strong>Statistiques :</strong> scipy.stats, statsmodels</li>
  <li><strong>Environnement :</strong> Jupyter Notebook</li>
</ul>
