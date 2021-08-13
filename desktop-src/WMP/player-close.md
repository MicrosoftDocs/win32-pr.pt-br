---
title: Método Player. Close
description: o método close libera Windows Media Player recursos.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Windows Media Player do método Close
- método close Windows Media Player, classe Player
- classe de jogador Windows Media Player, método close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29e68aed11b095dff80c8c91c88410f98b9a236bbcadcbff75da0fc0de392fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467876"
---
# <a name="playerclose-method"></a>Método Player. Close

o método **close** libera Windows Media Player recursos.

## <a name="syntax"></a>Sintaxe


```JScript
Player.close()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

esse método fecha o arquivo de mídia digital atual, não Windows Media Player ele mesmo.

## <a name="examples"></a>Exemplos

o exemplo a seguir cria um elemento de botão HTML que, quando clicado, interrompe a reprodução em Windows Media Player e libera os recursos em uso. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





