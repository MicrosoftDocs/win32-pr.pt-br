---
title: Controls. currentPosition
description: A propriedade currentPosition especifica ou recupera a posição atual no item de mídia em segundos desde o início.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. currentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763363"
---
# <a name="controlscurrentposition"></a>Controls. currentPosition

A propriedade **CurrentPosition** especifica ou recupera a posição atual no item de mídia em segundos desde o início.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**duplo**).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **CurrentPosition** para buscar uma posição fornecida pelo usuário. Um elemento de botão HTML é criado para executar o código JScript. Um elemento de entrada de texto HTML, chamado SETPOSITION, foi criado para aceitar um valor, em segundos, do usuário. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





