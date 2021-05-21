# custom-woocommerce-sorting
This is a custom sorting of Woocommerce products based on Stock Status and On Sale/ Without Sale

<pre>
1. For each product, Total point is calculated based on the following criteria and is saved under a meta field.
2. For example, if a product is "In Backorder" and it is "With Sale", that particular product will have 4 ( 3+0 ) Points
</pre>
# pointing-system

<pre>
In Stock = 1
In backorder = 3
Out of stock = 5

++++++++++++++++

With Sale = 0
Without sale = 1


</pre>

# ordering

Here is the ordering based on points

<pre>
1# Product in stock with sale price  ( 1 Point )
2# Product in stock without sale price ( 2 Points )
3# Product in backorder with sale price ( 3 Points )
4# Product in backorder without sale price  ( 4 Points )
5# Product Out of stock with sale price ( 5 Points )
6# Product out of stock without sale price ( 6 Points )
</pre>


Query Params

<pre>
$newArg = array(
	'post_type' => 'product',
	'meta_key'  => 'hbel_sort_point',   // Where Points are saved
	'orderby'    => 'meta_value_num',
        'order'      => 'ASC',	
);
</pre>

# use-case

Simply set the "Default product sorting" option present under <strong>Customizer -> Product Catalog</strong> to "Sort by Stock + Sale"


   
