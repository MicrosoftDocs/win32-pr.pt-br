---
title: Evento Player.MouseMove
description: O evento MouseMove ocorre quando o ponteiro do mouse é movido. | Evento Player.MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Evento MouseMove Windows Media Player
- Evento MouseMove Windows Media Player , classe Player
- Classe player Windows Media Player evento , MouseMove
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb864e2a8bf686bd39f2d44ba8f5558516d72034f606579a79c76a5d86ab3990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338092"
---
# <a name="playermousemove-event"></a>Evento Player.MouseMove

O **evento MouseMove** ocorre quando o ponteiro do mouse é movido.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nButton* 
</dt> <dd>

**Número** (**int**) especificando um campo de bits com bits correspondentes ao botão esquerdo (bit 0), botão direito (bit 1) e botão central (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que alguns, todos ou nenhum dos botões são pressionados.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) especificando um campo de bits com os bits menos significativos correspondentes à tecla SHIFT (bit 0), à tecla CTRL (bit 1) e à tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.

</dd> <dt>

*Fx* 
</dt> <dd>

**Number** (**long**) especificando a coordenada x do ponteiro do mouse em relação ao canto superior esquerdo do controle.

</dd> <dt>

*Fy* 
</dt> <dd>

**Number** (**long**) especificando a coordenada y do ponteiro do mouse em relação ao canto superior esquerdo do controle.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





