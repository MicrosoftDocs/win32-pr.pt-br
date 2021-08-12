---
title: Evento Player.MediaError
description: O evento MediaError ocorre quando o objeto Media tem uma condição de erro.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Eventos MediaError Windows Media Player
- Evento MediaError Windows Media Player , classe Player
- Classe player Windows Media Player evento , MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572836"
---
# <a name="playermediaerror-event"></a>Evento Player.MediaError

O **evento MediaError** ocorre quando o **objeto Media** tem uma condição de erro.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaObject* 
</dt> <dd>

**Objeto de** mídia que tem uma condição de erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





