---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMThirdPartyUpdateCategory

## SYNOPSIS

Use this cmdlet to modify third-party update categories.

## SYNTAX

### SearchByName (Default)
```
Set-CMThirdPartyUpdateCategory [[-CatalogName] <String>] [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValue
```
Set-CMThirdPartyUpdateCategory -InputObject <IResultObject> [-Id <String>] [-Name <String>]
 [-ParentId <String>] [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Set-CMThirdPartyUpdateCategory [[-CatalogId] <String>] [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCategory
```
Set-CMThirdPartyUpdateCategory [-Category] <IResultObject[]> [-PublishOption <PublishOptionType>]
 [-EnableCategory <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to modify third-party update categories.

## EXAMPLES

### Example 1

```powershell
Set-CMThirdPartyUpdateCategory -Catalog $catalog -Id $categoryId -PublishOption $publishOption -EnableCategories $true
$catalog | Set-CMThirdPartyUpdateCategory -Name $categoryName -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogId $catalogId -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogName $catalogName -Name $categoryName -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -Categories $categories -PublishOption $publishOption -EnableCategories $true
```

## PARAMETERS

### -CatalogId

Specify the ID of the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchById
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CatalogName

Specify the name of the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Category

Specify an object for the the third-party update catalog category.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByCategory
Aliases: Categories

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCategory

Enable the catagory for the third-party update catalog.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

Specify the category ID for the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the third-party update catalog.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Catalog

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the category name for the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentId

Specify the parent ID of the the third-party update catalog category.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByValue, SearchById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishOption

```yaml
Type: PublishOptionType
Parameter Sets: (All)
Aliases:
Accepted values: Skip, MetadataOnly, FullContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_ISVCatalogCategories

## NOTES

## RELATED LINKS