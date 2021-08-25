---
title: Propriedade Command. TooltipDescription
description: Representa uma descrição da dica de ferramenta.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- propriedade Command. TooltipDescription da faixa de Windows
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933206"
---
# <a name="commandtooltipdescription-property"></a>Propriedade Command. TooltipDescription

Representa uma descrição da dica de ferramenta.

## <a name="usage"></a>Uso

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Descrição                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Strings**](windowsribbon-element-string.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).

**Command. TooltipDescription** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.

 

O comprimento máximo é não associado.

Se nenhum valor for fornecido para **Command. TooltipDescription**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.

> [!Note]  
> Se **Command. TooltipDescription** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.

 

O **comando. TooltipDescription** só dá suporte ao alinhamento à esquerda.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. TooltipDescription** .


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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





