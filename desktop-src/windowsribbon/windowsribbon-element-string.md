---
title: Elemento String
description: Representa um recurso de cadeia de caracteres.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- elemento String Windows faixa de Ribbon
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630952"
---
# <a name="string-element"></a>Elemento String

Representa um recurso de cadeia de caracteres.

## <a name="usage"></a>Uso

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
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
<td><strong>Conteúdo</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>A ID de recurso exclusiva. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>O símbolo de recurso para a cadeia de caracteres.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos ou sublinhados.<br/> O comprimento máximo é de 100 caracteres.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Descrição                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String. Content**](windowsribbon-element-string-content.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Comando. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**comando. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) elemento.

A definição da cadeia de caracteres é adicionada ao arquivo de cabeçalho da faixa de faixas, por exemplo, `#define strSave 59999` .

A cadeia de caracteres é adicionada a uma tabela de cadeia de caracteres no arquivo de recurso da faixa de lista, em que um nome e uma ID são gerados pela estrutura da faixa de faixas, se nenhum for declarado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração de **cadeia de caracteres** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Informações do elemento

- **sistema mínimo com suporte**: Windows 7 
- **Pode estar vazio**: não



 

 





