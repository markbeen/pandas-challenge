# pandas-challenge

## I found this exercise pretty challenging. That said, learning how to move data around using Pandas is a critical skill I need to learn. Here are some important notes regarding Pandas:

<ol>
    <li> You can reference series with dot notation, rather than using brackets (i.e. ['series']). </li>    
    <li> I found a couple of solutions to add percent dollar signs ("$") to all values of a data series: 
        <ol type="a">
            <li>%: pd.options.display.float_format = '{:,.2f}%'.format</li>
            <li>$: pd.options.display.float_format = '${:,.2f}'.format</li>
            <li>reset format: pd.reset_option('display.float_format')</li>
        </ol>
        However, the options listed above were not ideal because they applied the format to all columns (i.e. series). Therefore, I found a function on the web that applied a numbering format only on values passed in. This seems like a better solution:
        <ol type="a">
              <li>def format(x):
        return "${:.2f}".format(x)</li>
        </ol>
    <li>groupby is very powerful when extracting specific rows associated with a value within a column. groupby is how I extracted most of the data for that latter exercises of the homework.</li>
    <li>sort_values can be used to sort a dataframe according to values within a specific series.</li>
    <li>set_index can be used to set the index column of a dataframe.</li>
    	<ol type="a">
            <li>Use inplace=True to write over the dataframe that was passed in.</li>
            <li>Use append=True to keep old index</li>
    	</ol><li> pd.cut was used to bin the data. I passed in my own bins. From what I understand, pd.qcut can be used to also bin the data, but it does so calculating the size of each bin so that each bin has roughly the same number of data points. </li></ol>



Finally, three observable trends in the data include:

<ol>
    <li>Heroes of Pymoli is overwhelming popular with players between the ages of 20 and 24.</li>
    <li>Heroes of Pymoli is overwhelming popular with male players. 84% of all players are male, followed by females (14%) and other/non-disclosed (1.91%)</li>
    <li>While collectively, males outspend females/others, the latter groups are willing to spend more per purchase. This statement is based on gender differences beteween the Average Total Price and the Average PUrchase Price. If true, then the game maker should determine how to better tap into the female/other market.  </li>
</ol>

