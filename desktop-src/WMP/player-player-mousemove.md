---
title: Evento Player. MouseMove
description: O evento MouseMove ocorre quando o ponteiro do mouse é movido. | Evento Player. MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Evento MouseMove Windows Media Player
- Evento MouseMove Windows Media Player, classe Player
- Classe Player Windows Media Player, evento MouseMove
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
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765644"
---
# <a name="playermousemove-event"></a>Evento Player. MouseMove

O evento **MouseMove** ocorre quando o ponteiro do mouse é movido.

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

*Nnovo* 
</dt> <dd>

**Número** (**int**) que especifica um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que alguns, todos ou nenhum dos botões são pressionados.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.

</dd> <dt>

*Efeito* 
</dt> <dd>

**Número** (**longo**) que especifica a coordenada x do ponteiro do mouse em relação ao canto superior esquerdo do controle.

</dd> <dt>

*SAR* 
</dt> <dd>

**Número** (**longo**) que especifica a coordenada y do ponteiro do mouse em relação ao canto superior esquerdo do controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

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

 

 





