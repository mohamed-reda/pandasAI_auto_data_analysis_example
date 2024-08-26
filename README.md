# PandasAI Auto Data Analysis Example

## Overview

PandasAI simplifies data analysis through conversational queries using large language models (LLMs) combined with pandas
dataframes. This repository demonstrates how to use PandasAI for auto data analysis.

## Installation

To install the library:

```bash
pip install pandasai
```

## Features

1. **SmartDataframe**: Adds conversational features to pandas dataframes.
2. **SmartDatalake**: Handles multiple dataframes simultaneously.
3. **LLM Integration**: Supports various LLMs such as OpenAI, AzureOpenAI, and Google Vertex AI.
4. **Connectors**: Easily connect to data sources like MySQL, PostgreSQL, and Yahoo Finance.
5. **Agents**: Multi-turn conversational analysis with memory.
6. **Training**: Instructions and Q/A training to improve analysis accuracy.

## Example Usage

1. **SmartDataframe**:
   ```python
   from pandasai import SmartDataframe
   df = SmartDataframe(pandas_dataframe)
   df.chat("Show the top 5 countries by GDP")
   ```

2. **SmartDatalake**:
   ```python
   from pandasai import SmartDatalake
   lake = SmartDatalake([df1, df2])
   lake.chat("Which employee has the highest salary?")
   ```

Exmples of LLM integration:

   ```python
   agent.chat('Which are the top 5 countries by sales?')
```

```
China, United States, Japan, Germany, Australia
```

----

   ```python
   agent.chat(
    "What is the total sales for the top 3 countries by sales?"
)
```

```
The total sales for the top 3 countries by sales is 16500.
```

----

   ```python
   sdf.chat("Plot a histogram of the gdp by country, using a different color for each bar")
   ```

----

   ```python
   agent.chat("Who gets paid the most?")
   ```

```
Olivia gets paid the most.
```

----

   ```python
   agent.chat(
    "Plot the histogram of countries showing for each one the gd. Use different colors for each bar",
)
```

![Chart](/histogram-chart.png?raw=true)


----
