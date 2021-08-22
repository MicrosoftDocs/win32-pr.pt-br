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
ms.openlocfilehash: ed4a12671877cf0d4d8abdb77d169b0f13000bc564e6c1dc37e65bf6eccdf005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580761"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

A **propriedade SAMIStyle** especifica ou recupera o estilo de legenda fechada.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter várias definições de estilo de formato. Os estilos SAMI são definidos entre <STYLE> as marcas e </STYLE> no arquivo SAMI. Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere. Por exemplo:


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

 

 





