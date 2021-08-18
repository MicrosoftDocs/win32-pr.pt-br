---
title: Evento Player. Click
description: O evento de clique ocorre quando o usuário clica em um botão do mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Windows Media Player de eventos de clique
- Windows Media Player de evento de clique, classe de jogador
- Windows Media Player de classe do Player, evento de clique
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60e6368c6ccb70d0bc87c9fc2d1d99770b4fa36dfe957365d48a2e26c00a163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995926"
---
# <a name="playerclick-event"></a>Evento Player. Click

O evento de **clique** ocorre quando o usuário clica em um botão do mouse.

## <a name="syntax"></a>Sintaxe


```JScript
Player.Click(
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

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





