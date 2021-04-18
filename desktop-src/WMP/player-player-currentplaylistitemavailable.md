---
title: Evento Player. CurrentPlaylistItemAvailable
description: O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Evento CurrentPlaylistItemAvailable do Windows Media Player
- Evento CurrentPlaylistItemAvailable Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771526"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Evento Player. CurrentPlaylistItemAvailable

O evento **CurrentPlaylistItemAvailable** ocorre quando a playlist atual fica disponível.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Cadeia de caracteres** que contém o nome do item da playlist atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O nome da lista de reprodução atual pode ser usado para recuperar o objeto de **playlist** correspondente usando a *playlistcollection*. método **getByName** .

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





