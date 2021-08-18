---
title: Método Controls.previous
description: O método anterior define o item atual para o item anterior na playlist.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- método anterior Windows Media Player
- método anterior Windows Media Player classe , Controls
- Classe Controls Windows Media Player , método anterior
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f67dbc80fb731f32eefb36f2a0f66c852da3da69dbc6b7ae56c03ebafb06e07e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119325"
---
# <a name="controlsprevious-method"></a>Método Controls.previous

O **método** anterior define o item atual para o item anterior na playlist.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a playlist estiver na primeira entrada quando **anterior** for invocada, a última entrada na playlist se tornará a atual.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML BUTTON que usa **anterior** para mover para o item anterior na playlist atual. O **objeto** Player foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 





