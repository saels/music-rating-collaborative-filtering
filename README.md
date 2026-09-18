# 🎵 Music Rating Collaborative Filtering

## 💼 Business use case

Music services need to personalize very large catalogs from sparse listener feedback. Collaborative filtering can learn common taste patterns across users and songs, making it useful for candidate generation even when explicit content features are limited.

## 🎯 Principal objective

Construct a user-song rating matrix, withhold observed ratings for validation, and apply SoftImpute low-rank matrix completion. The completed scores are evaluated against an average-rating baseline.

## 🔎 Summary of takeaways

The stored evaluation reports **0.2789 out-of-sample R²** and **0.4789 in-sample R²**. The positive validation R² confirms that the model captures reusable preference structure, while the remaining gap suggests that rank selection and regularization could be improved.

In a live recommendation product, rating prediction would be only one layer of the system. I would add top-N ranking metrics, catalog coverage, diversity, time-aware validation, and cold-start strategies. The completed scores could then feed a broader ranking process that also accounts for freshness, popularity, and exploration.

## 🧭 Explore the code

The [notebook](https://github.com/saels/music-rating-collaborative-filtering/blob/2dda373b718836d76ea1a8976a23a944a0cd70c4/Music_rating_collaborative_filtering.ipynb) shows how sparse listener feedback is converted into a low-rank recommendation model. Check the code for the matrix-completion workflow, validation design, and the evaluation used to measure generalization.
