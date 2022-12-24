# Trading strategy program

## Usage

### To display intraday trading data 
1. Create object of class ScriptData.
```python
script_data = ScriptData()
```
2. Then fetch data in json form convert it into Pandas DataFrame and then display it by calling.
```python
script_data.fetch_intraday_data('GOOGL')
script_data.convert_intraday_data('GOOGL')
script_data['GOOGL']
```
3. Check wheather data of company is available or not in script_data using **in** operator.
```python
'GOOGL' in script_data
```

### To get average of intraday trading data
4. use function **indicator1** to display df with average close value of no. of rows.
    >df = Pandas DataFrame
    
    >timeperiod = No. of rows we want to get average of.   type:Int
```python
indicator1(df, timeperiod)
```
eg.
```python
indicator1(script_data['GOOGL'],timeperiod = 5)
```
### To get Buying and Selling Strategy
5. First create object of class **Strategy**
> script = name of stock.  type:str
```python
strategy = Strategy(script)
```
eg.
```python
strategy = Strategy('GOOGL')
```
6. Call method **get_script_data()** and **get_signals()** to return df with Buying and Selling Strategy 
```python
strategy.get_script_data()
strategy.get_signals()
```
