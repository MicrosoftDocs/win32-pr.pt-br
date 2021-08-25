---
title: Command.Id propriedade
description: Representa uma ID exclusiva para um Comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id propriedade Windows Faixa de Opções
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931606"
---
# <a name="commandid-property"></a>Command.Id propriedade

Representa uma ID exclusiva para um Comando.

## <a name="usage"></a>Uso

``` syntax
<Command.Id/>
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

Pode ocorrer no máximo uma vez para cada [**Comando**](windowsribbon-element-command.md).

A ID está associada a uma definição de Comando no arquivo de header da Faixa de Opções, por exemplo, `#define cmdSave 25003 /* Save */` .

Esse elemento contém um valor da união dos tipos *xs:positiveInteger* e *xs:string* restrito a um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusivo.

O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um [**elemento Command**](windowsribbon-element-command.md) com uma **Command.Id** de dados.


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



 

 





