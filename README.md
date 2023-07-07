# EndlessRecyclerVIewScrollListner


#MainActivity.kt

```
private val layoutManager = LinearLayoutManager(this)
private val scrollListener =
        object : EndlessRecyclerViewScrollListener(layoutManager) {
            override fun onLoadMore(page: Int, totalItemsCount: Int, view: RecyclerView) {
                // Triggered only when new data needs to be appended to the list
                // Add whatever code is needed to append new items to the bottom of the list
                Log.w("TAG", "onLoadMore: $page")
             if (page < totalNosOfPages)
                loadBookings(page)
            }
        }
```

#onCreate() 

```
 binding.rvCards.layoutManager = layoutManager
 binding.rvTracks.addOnScrollListener(scrollListener)
```
