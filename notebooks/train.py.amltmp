import argparse
import os
import pandas as pd
from azureml.core import Run

def main():
    parser = argparse.ArgumentParser()
    parser.add_argument('--input_data', type=str, help="Name of input dataset")
    args = parser.parse_args()

    run = Run.get_context()

    print(f"Loading dataset named: {args.input_data}")
    input_dataset = run.input_datasets[args.input_data]

    df = input_dataset.to_pandas_dataframe()

    print(f"Dataset Loaded with shape: {df.shape}")
    print