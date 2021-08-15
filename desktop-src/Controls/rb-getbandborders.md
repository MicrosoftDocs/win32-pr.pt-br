---
title: RB_GETBANDBORDERS mensagem (Commctrl.h)
description: Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área acessível em uma banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b07303c10ef6f466907b11cf0e100927f63480690e77ac3dcbe80df80af97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409708"
---
# <a name="rb_getbandborders-message"></a>Mensagem \_ GETBANDBORDERS RB

Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área acessível em uma banda.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da faixa para a qual as bordas serão recuperadas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que receberá as bordas da banda. Se o controle de barra de rebar tiver o estilo [**\_ BANDBORDERS do RBS,**](rebar-control-styles.md) cada membro dessa estrutura receberá o número de pixels, no lado correspondente da faixa, que constituem a borda. Se o controle de barra de rebar não tiver  o estilo **\_ RBS BANDBORDERS,** somente o membro esquerdo dessa estrutura receberá informações válidas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

