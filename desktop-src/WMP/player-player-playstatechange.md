---
title: Evento Player.PlayStateChange
description: O evento PlayStateChange ocorre quando há uma alteração na propriedade playState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Evento PlayStateChange Windows Media Player
- Evento PlayStateChange Windows Media Player , classe Player
- Classe player Windows Media Player evento , PlayStateChange
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
ms.openlocfilehash: 3995f7373984ae9e3b0e24f9f41390154326cfd87bd8589970dc76520c6efd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572522"
---
# <a name="playerplaystatechange-event"></a>Evento Player.PlayStateChange

O **evento PlayStateChange** ocorre quando há uma alteração na **propriedade playState.**

## <a name="syntax"></a>Sintaxe


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Newstate* 
</dt> <dd>

Number (**long**) que especifica o novo **playState.** Consulte [playState](player-playstate.md) para ver uma tabela de valores possíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

Windows Media Player não há garantia de que ocorram em nenhuma ordem específica. Além disso, nem todos os estados ocorrem necessariamente durante uma sequência de eventos. Você não deve escrever código que depende da ordem de estado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra um manipulador de eventos para o *Player*. **Evento playStateChange.** Um elemento de texto HTML, chamado "myText", exibe o novo estado de reprodução. O objeto player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> </dl>

 

 





