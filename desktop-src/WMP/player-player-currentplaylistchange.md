---
title: Evento Player. CurrentPlaylistChange
description: O evento CurrentPlaylistChange ocorre quando algo é alterado na playlist atual. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Windows Media Player de eventos CurrentPlaylistChange
- Windows Media Player de eventos CurrentPlaylistChange, classe Player
- classe de jogador Windows Media Player, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672ff739e60efe73e1d30670dec5bc956f9fdd56506464b036add6f52cc6fc34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338142"
---
# <a name="playercurrentplaylistchange-event"></a>Evento Player. CurrentPlaylistChange

O evento **CurrentPlaylistChange** ocorre quando algo é alterado na playlist atual.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*change* 
</dt> <dd>

**Número** (**longo**) indicando que tipo de alteração ocorreu na lista de reprodução. Consulte o *Player*. Evento **PlaylistChange** para uma tabela de valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento não ocorre quando uma playlist diferente se torna a playlist atual. Isso ocorre apenas quando uma alteração acontece na playlist atual, como um item de mídia que está sendo anexado à playlist.

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript atualiza o texto em um elemento HTML DIV, chamado PlItems, para exibir os nomes dos itens de mídia na playlist atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player. PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 





