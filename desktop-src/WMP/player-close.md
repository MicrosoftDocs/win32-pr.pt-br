---
title: Método Player. Close
description: O método Close libera recursos do Windows Media Player.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- fechar o método Windows Media Player
- método Close Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método Close
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
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790482"
---
# <a name="playerclose-method"></a>Método Player. Close

O método **Close** libera recursos do Windows Media Player.

## <a name="syntax"></a>Sintaxe


```JScript
Player.close()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método fecha o arquivo de mídia digital atual, não o Windows Media Player em si.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que, quando clicado, interrompe a reprodução no Windows Media Player e libera os recursos em uso. O objeto de **jogador** foi criado com ID = "Player".


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

 

 





