---
title: Propriedade SplitButton.ButtonItem
description: Representa um contêiner para um botão ou botão de alternância que expõe o comando padrão de um botão de divisão.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Propriedade SplitButton.ButtonItem Windows Ribbon
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49f316f7c740b434f761bbe4c00906c8f76b5027af9fcc87317af2a51960dab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840686"
---
# <a name="splitbuttonbuttonitem-property"></a>Propriedade SplitButton.ButtonItem

Representa um contêiner para um [botão ou](windowsribbon-controls-button.md) botão [de alternância](windowsribbon-controls-togglebutton.md) que expõe o comando padrão de um [botão dividir](windowsribbon-controls-splitbutton.md).

## <a name="usage"></a>Uso

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Descrição                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>             | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**SplitButton.**](windowsribbon-element-splitbutton.md)

Cada **SplitButton.ButtonItem** pode conter apenas um [**elemento filho Button**](windowsribbon-element-button.md) ou [**ToggleButton.**](windowsribbon-element-togglebutton.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [botão Dividir](windowsribbon-controls-splitbutton.md).

Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton.ButtonItem,** com um Grupo associado que funciona como o contêiner pai para o **elemento SplitButton.** [](windowsribbon-element-group.md)


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Esta seção de código mostra as declarações de controle [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton.ButtonItem.**


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle Dividir Botão](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





