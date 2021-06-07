---
title: Elemento QuickAccessToolbar
description: Representa a QAT (Barra de Ferramentas de Acesso Rápido), uma pequena barra de ferramentas que exibe atalhos para Comandos da Faixa de Opções.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Faixa de Opções do Windows do elemento QuickAccessToolbar
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443297"
---
# <a name="quickaccesstoolbar-element"></a>Elemento QuickAccessToolbar

Representa a [QAT (Barra](windowsribbon-controls-quickaccesstoolbar.md)de Ferramentas de Acesso Rápido), uma pequena barra de ferramentas que exibe atalhos para Comandos da Faixa de Opções.

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
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CustomizeCommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Insere um item command adicional no menu QAT.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
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
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada [**Ribbon.QuickAccessToolbar.**](windowsribbon-element-ribbon-quickaccesstoolbar.md)

Os itens no QAT podem ser adicionados ou removidos em tempo de executar.

Para consistência entre aplicativos de Faixa de Opções, é recomendável que o manipulador de comandos *CustomizeCommandName* iniciar uma caixa de diálogo de personalização de QAT.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para **o QuickAccessToolbar**.

Esta seção de código mostra a **declaração comando QuickAccessToolbar.**


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



Esta seção de código mostra a **declaração de controle QuickAccessToolbar.**


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

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Barra de Ferramentas de Acesso Rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





