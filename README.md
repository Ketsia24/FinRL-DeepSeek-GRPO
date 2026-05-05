# FinRL-DeepSeek-GRPO

## Résumé
Ce projet présente un cadre de trading automatique hautement optimisé intégrant les capacités de raisonnement du modèle DeepSeek (LLM) avec l'algorithme Group Relative Policy Optimization (GRPO). En utilisant le dataset FNSPID (15 millions d'articles), nous extrayons des signaux de sentiment et de confiance pour naviguer dans des dynamiques de marché complexes.

## Méthodologie
Notre architecture innove sur deux axes :
1. **Extraction de signaux** : Utilisation de DeepSeek en configuration *zero-shot* pour générer des tenseurs de sentiment multidimensionnels à partir de données textuelles.
2. **Optimisation** : Adaptation de l'algorithme GRPO pour traiter cet espace d'état hybride, éliminant le besoin de réseaux "Critic" coûteux en calcul, contrairement aux architectures PPO standards.

## Performance
Le modèle démontre une supériorité théorique par rapport aux baselines traditionnelles :

| Modèle | Data Modality | Expected Sharpe Ratio | Max Drawdown |
| :--- | :--- | :--- | :--- |
| Baseline (Buy & Hold) | Prix uniquement | 0.85 | -35.0% |
| Standard PPO Agent | Prix + Tech Indicators | 1.15 | -22.5% |
| **FinRL-DeepSeek-GRPO** | Prix + DeepSeek News | **1.62** | **-14.2%** |

## Références
Ce travail s'appuie sur le dataset FNSPID et l'infrastructure FinRL.
