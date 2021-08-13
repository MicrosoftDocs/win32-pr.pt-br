---
title: RB_PUSHCHEVRON mensagem (Commctrl.h)
description: Enviado para um controle de barra de rebar para enviar por push programaticamente uma divisa.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d095cd824970b7ea90541420274b204a1e2f63ce6e1218e62221741f572feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434966"
---
# <a name="rb_pushchevron-message"></a>Mensagem PUSH LTDRON de RB \_

Enviado para um controle de barra de rebar para enviar por push programaticamente uma divisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da faixa cuja divisa deve ser pressionada.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor de 32 bits definido pelo aplicativo. Ele será passado de volta para o aplicativo como o membro **lParamNM** da estrutura [**NMREBAR LTDRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que é passada com a notificação [RBN \_ CHEVRONPUSHED.](rbn-chevronpushed.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="remarks"></a>Comentários

Quando essa mensagem for enviada, o controle de barra de rebar enviará ao aplicativo um código de notificação [RBN \_ CHEVRONPUSHED,](rbn-chevronpushed.md) solicitando que ele exibe o menu de divisa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





