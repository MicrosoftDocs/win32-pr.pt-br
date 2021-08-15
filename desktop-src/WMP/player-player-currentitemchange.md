---
title: Evento Player. CurrentItemChange
description: O evento CurrentItemChange ocorre quando o Controls. currentItem é alterado.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Windows Media Player de eventos CurrentItemChange
- Windows Media Player de eventos CurrentItemChange, classe Player
- classe de jogador Windows Media Player, evento CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338121"
---
# <a name="playercurrentitemchange-event"></a>Evento Player. CurrentItemChange

O evento **CurrentItemChange** ocorre quando os *controles*. **currentItem** é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript demonstra um manipulador de eventos para o *Player*. evento **currentItemChange** . O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





