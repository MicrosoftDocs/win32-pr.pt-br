---
title: Método Controls.play
description: O método play faz com que o item de mídia atual comece a reproduzir ou retoma a reprodução de um item em pausa.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- método play Windows Media Player
- classe play method Windows Media Player , Controls
- Classe Controls Windows Media Player , método play
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
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997446"
---
# <a name="controlsplay-method"></a>Método Controls.play

O **método play** faz com que o item de mídia atual comece a reproduzir ou retoma a reprodução de um item em pausa.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.play()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se esse método for chamado durante o encaminhamento rápido ou o rebobinamento, o valor de *Configurações*. **rate** é definida como 1,0.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML BUTTON que usa **a reprodução** para reproduzir o item de mídia atual. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





