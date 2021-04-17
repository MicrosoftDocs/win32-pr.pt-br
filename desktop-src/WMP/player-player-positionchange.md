---
title: Evento Player. PositionChange
description: O evento PositionChange ocorre quando a posição atual do item de mídia é alterada.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Evento PositionChange do Windows Media Player
- Evento PositionChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797643"
---
# <a name="playerpositionchange-event"></a>Evento Player. PositionChange

O evento **PositionChange** ocorre quando a posição atual do item de mídia é alterada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oldPosition* 
</dt> <dd>

Número (**duplo**) especificando a posição antiga.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Número** (**duplo**) especificando a nova posição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento não é gerado rotineiramente durante a reprodução. Isso ocorre apenas quando algo altera ativamente a posição atual do item de mídia em execução, como o usuário que move o identificador de busca ou o código que especifica um valor para *controles*. **CurrentPosition**.

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
</dt> </dl>

 

 





