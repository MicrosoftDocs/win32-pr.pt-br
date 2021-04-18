---
title: Método Controls. Pause
description: O método pause pausa a reprodução do item de mídia. | Método Controls. Pause
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- Método Pause Windows Media Player
- Método Pause Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método pause
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811123"
---
# <a name="controlspause-method"></a>Método Controls. Pause

O método **Pause** pausa a reprodução do item de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.pause()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um arquivo é pausado, o Windows Media Player não fornece nenhum recurso do sistema, como o dispositivo de áudio.

Determinados tipos de mídia não podem ser pausados, como transmissões ao vivo. Para determinar se um determinado tipo de mídia pode ser pausado, use *controles*. **isdisponível (' pause ')**.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **Pause** para pausar a reprodução. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
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
</dt> <dt>

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> </dl>

 

 





