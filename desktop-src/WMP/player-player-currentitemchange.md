---
title: Evento Player. CurrentItemChange
description: O evento CurrentItemChange ocorre quando o Controls. currentItem é alterado.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Evento CurrentItemChange do Windows Media Player
- Evento CurrentItemChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentItemChange
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
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810879"
---
# <a name="playercurrentitemchange-event"></a>Evento Player. CurrentItemChange

O evento **CurrentItemChange** ocorre quando os *controles*. **currentItem** é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir demonstra um manipulador de eventos para o *Player*. evento **currentItemChange** . O objeto de **jogador** foi criado com ID = "Player".


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

 

 





