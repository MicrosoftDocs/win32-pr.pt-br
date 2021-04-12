---
title: Mensagem de RB_BEGINDRAG (commctrl. h)
description: Coloca o controle rebar no modo arrastar e soltar. Essa mensagem não faz com que uma \_ notificação RBN BEGINDRAG seja enviada.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Controles de RB_BEGINDRAG de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455537"
---
# <a name="rb_begindrag-message"></a>\_Mensagem BEGINDRAG RB

Coloca o controle rebar no modo arrastar e soltar. Essa mensagem não faz com que uma notificação [RBN \_ BEGINDRAG](rbn-begindrag.md) seja enviada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda que a operação de arrastar e soltar afetará.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contém as coordenadas de início do mouse. A coordenada horizontal está contida no LOWORD e a coordenada vertical está contida no HIWORD. Se você passar (**DWORD**)-1, o controle Rebar usará a posição do mouse na última vez em que o thread do controle chamou [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

As **mensagens \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)e [**RB \_ EndDrag**](rb-enddrag.md) permitem que você implemente uma interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para um controle rebar. Você envia a mensagem **RB \_ BEGINDRAG** em resposta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envia a mensagem de **\_ DRAGMOVE RB** em resposta [**a IDROPTARGET::D ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)e a mensagem **RB \_ endarraste** em resposta a [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

