---
title: Elemento Ribbon
description: Representa o controle da faixa de faixas na exibição da faixa de faixas.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- faixa de Windows de elemento da faixa de faixas
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70841866ec656dc840fb467d598cc42bf919283b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630912"
---
# <a name="ribbon-element"></a>Elemento Ribbon

Representa o controle da faixa de faixas na exibição da faixa de faixas.

## <a name="usage"></a>Uso

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
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
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> Menores<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> Médio<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Vários<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Usado para anotar o elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Qualquer sequência de zero ou mais caracteres.<br/> O comprimento máximo é não associado.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                         | Descrição                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Faixa de guia. guias**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada elemento [**Application. views**](windowsribbon-element-application-views.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para um modo de exibição de **faixa** de opções.


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Informações do elemento




* **sistema mínimo com suporte**: Windows 7
* **Pode estar vazio**: não



 

 





