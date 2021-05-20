# custom-woocommerce-sorting
This is a custom sorting of Woocommerce products based on Stock Status and On Sale/ Without Sale

The Idea is based on Pointing system and here it how it sorts the Woocommerce Products based on Pointing system

# pointing-system

In Stock = 1
In backorder = 3
Out of stock = 5


With Sale = 0
Without sale = 1

# ordering

1# Product in stock with sale price  ( 1 Point )
2# Product in stock without sale price ( 2 Points )
3# Product in backorder with sale price ( 3 Points )
4# Product in backorder without sale price  ( 4 Points )
5# Product Out of stock with sale price ( 5 Points )
6# Product out of stock without sale price ( 6 Points )

# use-case

Simply set the following parameters in Query args


<code>
$newArg = array(
			'post_type' => 'product',
			'meta_key'  => 'hbel_sort_point',   // Where Points are saved
			'orderby'    => 'meta_value_num',
      'order'      => 'ASC',	
);
</code>
	    
