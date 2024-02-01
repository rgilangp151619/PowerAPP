If(
    Value(txtqty_1.Text) = 0,
    Notify(
        "Please Input Order Qty!",
        NotificationType.Warning,
        5000
    ),
    Collect(
        Collection Name,
        {
            Item: ThisItem.ItemDescription,
            UoM: ThisItem.UoM,
            OrderQty: Value(txtqty_1.Text),
            BalanceQty: Value(balanceqty_1.Text),
            Billback: billback_1.Value
        }
    )
)
