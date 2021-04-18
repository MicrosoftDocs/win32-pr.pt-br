---
title: Evento Player. KeyPress
description: O evento KeyPress ocorre quando uma tecla é pressionada e liberada. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Evento KeyPress Windows Media Player
- Evento KeyPress Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791512"
---
# <a name="playerkeypress-event"></a>Evento Player. KeyPress

O evento **KeyPress** ocorre quando uma tecla é pressionada e liberada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nKeyAscii* 
</dt> <dd>

**Número** (**int**) especificando o código ANSI numérico padrão para o caractere.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento ocorre quando o pressionamento de tecla resulta em qualquer caractere de teclado imprimível, a tecla CTRL combinada com um caractere do alfabeto padrão ou um de alguns caracteres especiais e a tecla ENTER ou Backspace.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





