If(
    Form4_2.Mode = FormMode.Edit && DataCardValue52.Selected.Value = "Assigned to GA" && DataCardValue46.Selected.Value = "Consumable" || DataCardValue46.Selected.Value = "Others" && LookUp('List User',User().Email = Email,Role.Value="GA" || Role.Value = "Super User"),
    true,
    If(
        Form4_2.Mode = FormMode.Edit && DataCardValue52.Selected.Value = "Rejected" && DataCardValue46.Selected.Value = "Consumable" || DataCardValue46.Selected.Value = "Others" && LookUp('List User',User().Email = Email,Role.Value="GA" || Role.Value = "Super User"),true,false
)
)
