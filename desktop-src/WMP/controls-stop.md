---
title: Método Controls. Stop
description: O método Stop interrompe a reprodução do item de mídia. | Método Controls. Stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- método Stop Windows Media Player
- método Stop Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método Stop
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762090"
---
# <a name="controlsstop-method"></a>Método Controls. Stop

O método **Stop** interrompe a reprodução do item de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método faz com que o Windows Media Player libere os recursos do sistema que está usando, como o dispositivo de áudio. O item de mídia atual, no entanto, não é liberado.

Quando o jogador for interrompido, a faixa retrocederá até o início. Chamar **Play** começará a reprodução do clipe desde o início. Para interromper uma operação de reprodução sem alterar a posição atual, use o método **Pause** .

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **parar** para parar a reprodução. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
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

[**Controls. Pause**](controls-pause.md)
</dt> <dt>

[**Controles. Previous**](controls-previous.md)
</dt> </dl>

 

 





