---
title: Evento Player. MouseDown
description: O evento MouseDown ocorre quando o usuário pressiona um botão do mouse. | Evento Player. MouseDown
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- Evento MouseDown do Windows Media Player
- Evento MouseDown Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MouseDown
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29eb0c8aa5f6731f94d0e4c3b4ff967cb7819f42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764151"
---
# <a name="playermousedown-event"></a>Evento Player. MouseDown

O evento **MouseDown** ocorre quando o usuário pressiona um botão do mouse.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MouseDown(
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

**Número** (**int**) que especifica um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits é definido, indicando o botão que causou o evento.

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

 

 





