---
title: Propriedade Command.TooltipTitle
description: Representa um título de dica de ferramenta.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Propriedade Command.TooltipTitle Windows Faixa de Opções
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9050c97980b0ffa2c2c4828a8ac1d85dfbd1a40ed8330d144db2c0d3802524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710546"
---
# <a name="commandtooltiptitle-property"></a>Propriedade Command.TooltipTitle

Representa um título de dica de ferramenta.

## <a name="usage"></a>Uso

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Descrição                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**Comando**](windowsribbon-element-command.md).

**Command.TooltipTitle** pode conter um valor do tipo *xs:string* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML do Conjunto de Caracteres Universal (UCS) `&#xA;` para especificar uma quebra de linha.

 

O comprimento máximo não é desaconsudido.

Se nenhum valor for fornecido para **Command.TooltipTitle,** o elemento [**filho String**](windowsribbon-element-string.md) será necessário.

> [!Note]  
> Se **Command.TooltipTitle** contiver um valor e um elemento [**filho String,**](windowsribbon-element-string.md) String **tem** precedência.

 

**Command.TooltipTitle dá** suporte apenas ao alinhamento à esquerda.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um [**elemento Command**](windowsribbon-element-command.md) com uma **declaração Command.TooltipTitle.**


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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Dica de \_ ferramenta PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





