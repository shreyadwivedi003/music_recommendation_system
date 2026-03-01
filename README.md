## Music Recommendation System<br>
This repository contains a Python-based recommendation engine designed to suggest songs to users using two primary approaches: Popularity-based filtering and Item-similarity-based collaborative filtering.

## Project Overview
The goal of this project is to analyze user listening history and song metadata to provide personalized music recommendations. The system is built using pandas for data manipulation and a custom module Recommenders to handle the engine logic.

### Datasets
The project utilizes two main data sources:

triplets_file.csv: Contains user listening data, including user_id, song_id, and listen_count.

song_data.csv: Contains song metadata, including song_id, title, release (album), artist_name, and year.

## Features
Data Preprocessing:

Merges listening history with song metadata.

Creates a unified song feature by combining the title and artist name.

Subset sampling (first 50,000 rows) to optimize computational performance.

Popularity Recommender: A "one-size-fits-all" model that recommends the most popular songs based on global listen counts.

Item Similarity Recommender: A personalized model that calculates a co-occurrence matrix to find songs similar to those a user has already listened to.

Search Functionality: Capability to input a specific song and receive a list of related tracks based on item similarity scores.

## Workflow
Environment Setup: Imports pandas, numpy, and the custom Recommenders library.

Data Integration: Merges the two datasets on song_id and removes duplicates.

Exploratory Analysis: Aggregates data to calculate the percentage of total listen counts per song.

Model Training:

Initializes popularity_recommender_py.

Initializes item_similarity_recommender_py.

Recommendation Generation: Demonstrates recommendations for specific users (e.g., users at index 5 and 70) and specific song queries.

## Key Results
The system successfully identifies top-performing tracks such as:

Sehr kosmisch - Harmonia

Undo - Björk

Dog Days Are Over (Radio Edit) - Florence + The Machine

## Prerequisites
To run this notebook, you will need the following Python libraries:

pandas

numpy

os

Recommenders (This is a local Python script expected to be in the project directory).
