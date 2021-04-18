---
title: Propriedade Command. Symbol
description: Representa o nome de um comando que pode ser referenciado externamente.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Faixa de das propriedades do Windows do comando. Symbol
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764514"
---
# <a name="commandsymbol-property"></a>Propriedade Command. Symbol

Representa o nome de um [**comando**](windowsribbon-element-command.md) que pode ser referenciado externamente.

## <a name="usage"></a>Uso

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).

O símbolo é associado a uma definição de comando no arquivo de cabeçalho da faixa de, por exemplo, `#define cmdSave 25003 /* Save */` .

Esse elemento contém um valor do tipo *xs: String*.

O valor é restrito a uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos e sublinhados.

O comprimento máximo é de 100 caracteres.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. Symbol** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





