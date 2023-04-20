---
sidebar_position: 1
---

# Your First Query

The simplest way to create and run a query is to use the IDE: [https://graphql.bitquery.io/ide](https://graphql.bitquery.io/ide).
You first have to [register](../ide/login), and the IDE window will open.

If IDE points to the default endpoint https://graphql.bitquery.io, you have to change it to the new endpoint
https://streaming.bitquery.io/graphql. Bookmark the link to open IDE with the
correct URL: [https://graphql.bitquery.io/ide?endpoint=https://streaming.bitquery.io/graphql](https://graphql.bitquery.io/ide?endpoint=https://streaming.bitquery.io/graphql)

If you did everything correctly, you will 
see the grey triangle in the middle of the screen to run the query.

Query editor is in the center of the screen, and you can use handy Ctrl-Space key
combination to see all possible options that you can enter at edit point. On the empty 
editor, it will show the drop-down list:

![IDE context menu](https://github.com/mayowaolatunji/streaming-data-platform-docs/blob/3f6bd0288913b4ee69ab3b63d1ba9de07876d0b0/static/img/ide/context_menu.png)

So you can type the query using hints from IDE. As example, you can
query the latest 10 blocks on ETH network:

```graphql
{
  EVM(network: eth) {
    Blocks(limit: {count: 10}) {
      Block {
        Number
        Time
      }
    }
  }
}
```

After you created a query, the run triangle button will appear to be green, 
and you can press it now to see the results:

![IDE query execution](https://github.com/mayowaolatunji/streaming-data-platform-docs/blob/bfff9241116a8f173b867b141211f49617a1a461/static/img/ide/query_execution.png)


