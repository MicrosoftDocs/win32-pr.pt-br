---
title: Elemento QuickAccessToolbar
description: Representa a barra de ferramentas de acesso rápido (QAT), uma pequena barra de ferramentas que exibe atalhos para comandos da faixa de das faixas.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Faixa de QuickAccessToolbar do elemento do Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365497"
---
# <a name="quickaccesstoolbar-element"></a>Elemento QuickAccessToolbar

Representa a [barra de ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md), uma pequena barra de ferramentas que exibe atalhos para comandos da faixa de das faixas.

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
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
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CustomizeCommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Insere um item de comando adicional no menu QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                                   | Descrição                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).

Os itens no QAT podem ser adicionados ou removidos em tempo de execução.

Para fins de consistência em aplicativos de faixa de faixas, é recomendável que o manipulador de comandos *CustomizeCommandName* inicie uma caixa de diálogo de personalização qat.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o **QuickAccessToolbar**.

Esta seção de código mostra a declaração de comando **QuickAccessToolbar** .


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



Esta seção de código mostra a declaração de controle **QuickAccessToolbar** .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





