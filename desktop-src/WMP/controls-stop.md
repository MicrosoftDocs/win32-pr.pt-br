---
title: Método Controls. Stop
description: O método Stop interrompe a reprodução do item de mídia. | Método Controls. Stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- Windows Media Player do método Stop
- método stop Windows Media Player, classe Controls
- classe Controls Windows Media Player, método stop
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
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580155"
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

esse método faz Windows Media Player liberar os recursos do sistema que está usando, como o dispositivo de áudio. O item de mídia atual, no entanto, não é liberado.

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

 

 





