---
title: Método Controls. Play
description: O método Play faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- método play Windows Media Player
- método play Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761475"
---
# <a name="controlsplay-method"></a>Método Controls. Play

O método **Play** faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.play()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se esse método for chamado durante o encaminhamento rápido ou o retrocesso, o valor das *configurações*. a **taxa** é definida como 1,0.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **Play** para reproduzir o item de mídia atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
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

 

 





