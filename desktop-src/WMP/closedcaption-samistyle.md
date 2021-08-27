---
title: ClosedCaption.SAMIStyle
description: A propriedade SAMIStyle especifica ou recupera o estilo de legenda fechada.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption.SAMIStyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bd45977e3d433239e74aee21def913b640fad12
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882179"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

A **propriedade SAMIStyle** especifica ou recupera o estilo de legenda fechada.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter várias definições de estilo de formato. Os estilos SAMI são definidos entre &lt; o STYLE e as marcas no arquivo &gt; </STYLE> SAMI. Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere. Por exemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Isso especifica um estilo que produz uma fonte específica.

Se nenhum estilo SAMI for especificado, o primeiro estilo definido no arquivo SAMI será usado por padrão.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir cria um elemento HTML SELECT que usa *closedCaption*. **SAMIStyle** para alterar a aparência do texto de legenda fechado. O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





