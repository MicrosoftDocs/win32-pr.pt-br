---
title: ClosedCaption.captioningID
description: A propriedade captioningID especifica ou recupera o nome do elemento que exibe a legenda.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption.captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da667e5479cc33312375920c1d573f0e2c19607b2399ff6f4fe34b130ca61e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580984"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

A **propriedade captioningID** especifica ou recupera o nome do elemento que exibe a legenda.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

O nome do elemento especificado pode ser qualquer elemento HTML na página da Web, desde que ele seja compatível com o atributo innerHTML. Se a página da Web contiver vários quadros, o nome do elemento só poderá se referir a um elemento no mesmo quadro que o controle Player.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

O exemplo de JScript Microsoft a seguir *usa ClosedCaption*. **captioningID** para escolher a área de uma página da Web usada para exibir legendas. Dois elementos DIV HTML foram criados, com ID = CC1 e ID = CC2, respectivamente. O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

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

 

 





