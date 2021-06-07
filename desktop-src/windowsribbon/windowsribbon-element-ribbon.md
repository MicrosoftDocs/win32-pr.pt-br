---
title: Elemento Ribbon
description: Representa o controle de faixa de opções na Exibição da Faixa de Opções.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Faixa de Opções do elemento Ribbon do Windows
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444997"
---
# <a name="ribbon-element"></a>Elemento Ribbon

Representa o controle de faixa de opções na Exibição da Faixa de Opções.

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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><dt><span></span><span></span><strong></strong> (Pequeno)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (Médio)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Usado para anotar o elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Qualquer sequência de zero ou mais caracteres.<br/> O comprimento máximo não ébounded.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                         | Descrição                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application.Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada [**elemento Application.Views.**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para uma **Exibição** da Faixa de Opções.


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




* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



 

 





