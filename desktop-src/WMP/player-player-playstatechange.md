---
title: Evento Player. PlayStateChange
description: O evento PlayStateChange ocorre quando há uma alteração na propriedade PlayState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Evento PlayStateChange do Windows Media Player
- Evento PlayStateChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790592"
---
# <a name="playerplaystatechange-event"></a>Evento Player. PlayStateChange

O evento **PlayStateChange** ocorre quando há uma alteração na propriedade **PlayState** .

## <a name="syntax"></a>Sintaxe


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewState* 
</dt> <dd>

Número (**longo**) que especifica o novo **PlayState**. Consulte [PlayState](player-playstate.md) para obter uma tabela de valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra um manipulador de eventos para o *Player*. evento **playStateChange** . Um elemento de texto HTML, chamado "MyText", exibe o novo estado de reprodução. O objeto de jogador foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
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

[**Player. PlayState**](player-playstate.md)
</dt> </dl>

 

 





