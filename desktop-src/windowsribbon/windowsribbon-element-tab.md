---
title: Elemento Tab
description: Representa uma guia principal ou contextual.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Elemento Tab Windows Ribbon
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 349004f65713160acc75bdb6f77765ad9f0c3034
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625952"
---
# <a name="tab-element"></a>Elemento Tab

Representa uma [guia principal](windowsribbon-controls-tab.md) [ou contextual.](windowsribbon-controls-tabgroup.md)

## <a name="usage"></a>Uso

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Válido somente se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> for o elemento pai.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                         | Descrição                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Grupo**](windowsribbon-element-group.md)<br/>                         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**Tabgroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer pelo menos uma vez para cada [**elemento Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) [**ou TabGroup.**](windowsribbon-element-tabgroup.md)

**A guia** dá suporte [aos modos de aplicativo](ribbon-applicationmodes.md).

Se [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) estiver presente para o elemento **Tab,** uma entrada para cada elemento [**Group**](windowsribbon-element-group.md) e seu tamanho ideal será necessária em **ScalingPolicy.IdealSizes**.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o **elemento Tab.**

Esta seção de código mostra as declarações **comando tab** para uma **guia** Página Início.


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



Esta seção de código mostra as **declarações de controle** Tab.


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>Informações do elemento

- **Sistema mínimo com suporte:** Windows 7 
- **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle guia](windowsribbon-controls-tab.md)
</dt> <dt>

[Controle De grupo de guias](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

