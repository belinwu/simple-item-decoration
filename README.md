#SimpleItemDecoration

**Currently in active development**

**SimpleItemDecoration** is a simple library for adding dividers and offsets to Android's `RecyclerView` using `RecyclerView.ItemDecoration`.

It can be used to add both interior dividers and start/end offsets to RecyclerViews using `LinearLayoutManager` or `GridLayoutManager`.

###Usage

All of the ItemDecorations included can be added to your RecyclerView by calling `RecyclerView#addItemDecoration()`, passing in your desired ItemDecoration as a parameter.

####DividerItemDecoration

`DividerItemDecoration` is used to add interior dividers to a `RecyclerView` using a `LinearLayoutManager`. 

Its constructor takes in your preferred divider as a `Drawable`.

```java
Drawable dividerDrawable = getResources().getDrawable(R.drawable.divider);

recyclerView.addItemDecoration(new DividerItemDecoration(dividerDrawable));
```

####StartOffsetItemDecoration

`StartOffsetItemDecoration` is used to add an offset to the start of a `RecyclerView` using a `LinearLayoutManager`. 
If the `RecyclerView` is oriented vertically, the offset will be added to the top of the `RecyclerView`.
If the `RecyclerView` is oriented horizontally, the offset will be added to the lefthand side of the `RecyclerView`.

Its constructor takes in your preferred offset in pixels.

```java
int offsetPx = 10;

recyclerView.addItemDecoration(new StartOffsetItemDecoration(offsetPx));
```

####EndOffsetItemDecoration

`EndOffsetItemDecoration` is used to add an offset to the end of a `RecyclerView` using a `LinearLayoutManager`. 
If the `RecyclerView` is oriented vertically, the offset will be added to the bottom of the `RecyclerView`.
If the `RecyclerView` is oriented horizontally, the offset will be added to the righthand side of the `RecyclerView`.

Its constructor takes in your preferred offset in pixels.

```java
int offsetPx = 10;

recyclerView.addItemDecoration(new EndOffsetItemDecoration(offsetPx));
```

####GridDividerItemDecoration

`GridDividerItemDecoration` is used to add interior dividers to a `RecyclerView` using a `GridLayoutManager`. 

Its constructor takes in your preferred horizontal and vertical dividers, along with the number of columns in the grid.

```java
Drawable horizontalDividerDrawable = getResources().getDrawable(R.drawable.divider_horizontal);
Drawable verticalDividerDrawable = getResources().getDrawable(R.drawable.divider_vertical);
int numColumns = 2;

recyclerView.addItemDecoration(new GridDividerItemDecoration(horizontalDividerDrawable, verticalDividerDrawable, numColumns));
```

####GridTopOffsetItemDecoration

`GridTopOffsetItemDecoration` is used to add an offset to the top of a `RecyclerView` using a `GridLayoutManager`. 

Its constructor takes in your preferred offset in pixels and the number of columns in the grid.

```java
int offsetPx = 10;
int numColumns = 2;

recyclerView.addItemDecoration(new GridTopOffsetItemDecoration(offsetPx, numColumns));
```

####GridBottomOffsetItemDecoration

`GridBottomOffsetItemDecoration` is used to add an offset to the bottom of a `RecyclerView` using a `GridLayoutManager`. 

Its constructor takes in your preferred offset in pixels and the number of columns in the grid.

```java
int offsetPx = 10;
int numColumns = 2;

recyclerView.addItemDecoration(new GridBottomOffsetItemDecoration(offsetPx, numColumns));
```
