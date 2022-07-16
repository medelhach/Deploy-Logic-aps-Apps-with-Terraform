```
# Section 1
resource "azurerm_resource_group" "example" {
  name     = "workflow-resources"
  location = "West Europe"
}


# Section 2
resource "azurerm_logic_app_workflow" "example" {
  name                = "workflow1"
  location            = azurerm_resource_group.example.location
  resource_group_name = azurerm_resource_group.example.name
}

```

* We create a resource section where we define our resource group , the name and The resource .
* And the next section we create a logic apps resource we specify the the name and the location and 
resource group name . 
