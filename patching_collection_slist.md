ForAll(
    Galleryname.AllItems,
    Patch(
        Sharepoint Data,
        Defaults(Sharepoint Data),
        {
            Title: txtdocid_1.Text,
            'Project Name': projectdropdown_1.SelectedText.'Project Name',
            ItemDescription: ThisRecord.Item,
            'Order Qty': ThisRecord.OrderQty,
            UoM: ThisRecord.UoM,
            'Balance Stock': ThisRecord.BalanceQty,
            'Request Date': todaydate_1.SelectedDate,
            'Request Need By': requestforperiod_1.SelectedDate,
            'Billback?': If(ThisRecord.Billback=true,"Yes","No"),
            'GA Site': gasite_1.Text
        }
    )
)
