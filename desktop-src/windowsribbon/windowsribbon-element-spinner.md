---
title: Elemento Spinner
description: Representa um controle Spinner.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Faixa de Opções do Windows do elemento Spinner
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444807"
---
# <a name="spinner-element"></a>Elemento Spinner

Representa um [controle Spinner.](windowsribbon-controls-spinner.md)

## <a name="usage"></a>Uso

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
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
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Grupo**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**ou Group.**](windowsribbon-element-group.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [Spinner](windowsribbon-controls-spinner.md).

Esta seção de código mostra as declarações de Comando do **Spinner,** com um elemento [**Group**](windowsribbon-element-group.md) que funciona como o contêiner pai para o **elemento Spinner.**


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



Esta seção de código mostra as **declarações de controle Spinner.**


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a>Informações do elemento

- **Sistema mínimo com suporte:** Windows 7 
- **Pode estar vazio:** Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de rotação](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





