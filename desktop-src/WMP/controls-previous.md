---
title: Método Controls. Previous
description: O método anterior define o item atual para o item anterior na lista de reprodução.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- método anterior Windows Media Player
- método anterior Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método anterior
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
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760270"
---
# <a name="controlsprevious-method"></a>Método Controls. Previous

O método **anterior** define o item atual para o item anterior na lista de reprodução.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a lista de reprodução estiver na primeira entrada quando a **anterior** for invocada, a última entrada na lista de reprodução se tornará a atual.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **Previous** para mover para o item anterior na playlist atual. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controles. Next**](controls-next.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> </dl>

 

 





