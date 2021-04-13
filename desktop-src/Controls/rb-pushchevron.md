---
title: Mensagem de RB_PUSHCHEVRON (commctrl. h)
description: Enviado a um controle rebar para enviar por push programaticamente uma divisa.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Controles de RB_PUSHCHEVRON de mensagens do Windows
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
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499540"
---
# <a name="rb_pushchevron-message"></a>\_Mensagem PUSHCHEVRON RB

Enviado a um controle rebar para enviar por push programaticamente uma divisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da faixa cuja divisa deve ser enviada por push.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor de 32 bits definido pelo aplicativo. Ele será passado de volta para o aplicativo como o membro **lParamNM** da estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que é passada com a notificação [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

Quando essa mensagem é enviada, o controle rebar enviará ao aplicativo um código de notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , solicitando que ele exiba o menu de divisa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





