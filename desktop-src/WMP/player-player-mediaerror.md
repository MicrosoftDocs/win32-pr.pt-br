---
title: Evento Player. MediaError
description: O evento MediaError ocorre quando o objeto de mídia tem uma condição de erro.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Evento MediaError do Windows Media Player
- Evento MediaError Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaError
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
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810827"
---
# <a name="playermediaerror-event"></a>Evento Player. MediaError

O evento **MediaError** ocorre quando o objeto de **mídia** tem uma condição de erro.

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

Objeto de **mídia** que tem uma condição de erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





