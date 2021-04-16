---
title: Método Player. openPlayer
description: O método openPlayer abre o Windows Media Player usando a URL especificada. | Método Player. openPlayer
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- método openPlayer Windows Media Player
- método openPlayer Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método openPlayer
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
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773084"
---
# <a name="playeropenplayer-method"></a>Método Player. openPlayer

O método **openPlayer** abre o Windows Media Player usando a URL especificada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que representa a URL do item de mídia a ser reproduzido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método inicia o Windows Media Player com a URL especificada definida como o item de mídia atual. Se o Player foi fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário. Caso contrário, o Player será aberto no modo completo.

Se esse método for chamado de um controle PlayerActiveX de mídia do Windows incorporado no modo remoto, seu comportamento será idêntico ao *PlayerApplication*. método **switchToPlayerApplication** .

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





