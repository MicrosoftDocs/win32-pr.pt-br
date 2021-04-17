---
title: ClosedCaption. SAMIstyle
description: A propriedade SAMIstyle especifica ou recupera o estilo de legenda oculta.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIstyle Windows Media Player
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
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762093"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption. SAMIstyle

A propriedade **samistyle** especifica ou recupera o estilo de legenda oculta.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter várias definições de estilo de formato. Os estilos SAMI são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami. Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere. Por exemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Isso especifica um estilo que produz uma fonte específica.

Se nenhum estilo SAMI for especificado, o primeiro estilo definido no arquivo SAMI será usado por padrão.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir cria um elemento HTML SELECT que usa *closedCaption*. **Samistyle** para alterar a aparência do texto da legenda oculta. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





