# Social Metric Calculator

This repository contains data and a methodology for calculating a normalized influence score.

## Methodology

To calculate the Normalized Influence Score for a specific user, follow these steps:

1.  For each post by the user, calculate a 'Raw Impact Score'. The formula is: `(comments * 5) + (shares * 10)`.
2.  Calculate the average 'Raw Impact Score' across all of that user's posts.
3.  Calculate a 'Content Originality Factor'. The formula is: `(total_posts_by_user / total_posts_in_dataset)`.
4.  The final 'Normalized Influence Score' is the result of: `(Average Raw Impact Score * Content Originality Factor) + average_likes_per_impression`.
    - Note: The `average_likes_per_impression` is calculated as `total_likes / total_impressions` for that user only.
