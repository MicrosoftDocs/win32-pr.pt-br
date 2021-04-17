---
title: Evento Player. MediaChange
description: O evento MediaChange ocorre quando um item de mídia é alterado. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Evento MediaChange do Windows Media Player
- Evento MediaChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763333"
---
# <a name="playermediachange-event"></a>Evento Player. MediaChange

O evento **MediaChange** ocorre quando um item de mídia é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* 
</dt> <dd>

O objeto de **mídia** que representa o item que foi alterado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa um elemento HTML DIV, chamado MEDIANAME, para exibir o nome do item de mídia atual. O código atualiza o texto na DIV com cada ocorrência do evento **mediaChange** . O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
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
</dt> </dl>

 

 





