---
title: Método Player.openPlayer
description: O método openPlayer é aberto Windows Media Player usando a URL especificada. | Método Player.openPlayer
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Método openPlayer Windows Media Player
- método openPlayer Windows Media Player , classe Player
- Classe player Windows Media Player , método openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42245ec29f7d7caeac17f116d1f592f74f10ba95716d5d16734ecd21bbcbb60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747564"
---
# <a name="playeropenplayer-method"></a>Método Player.openPlayer

O **método openPlayer** é aberto Windows Media Player usando a URL especificada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que representa a URL do item de mídia a ser reproduzir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é Windows Media Player com a URL especificada definida como o item de mídia atual. Se o Player tiver sido fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário. Caso contrário, o Player será aberto no modo completo.

Se esse método for chamado de um controle Windows Media PlayerActiveX inserido no modo remoto, seu comportamento será idêntico ao *PlayerApplication*. **Método switchToPlayerApplication.**

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





