---
title: Mensagem de RB_DRAGMOVE (commctrl. h)
description: Atualiza a posição de arrastar no controle rebar após uma mensagem BEGINDRAG de RB anterior \_ .
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Controles de RB_DRAGMOVE de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918784"
---
# <a name="rb_dragmove-message"></a>\_Mensagem DRAGMOVE RB

Atualiza a posição de arrastar no controle rebar após uma mensagem [**\_ BEGINDRAG de RB**](rb-begindrag.md) anterior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contém as novas coordenadas do mouse. A coordenada horizontal está contida no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e a coordenada vertical está contida no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se você passar (DWORD)-1, o controle Rebar usará a posição do mouse na última vez em que o thread do controle chamou [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ARRASTAR para a RB \_**](rb-enddrag.md)
</dt> </dl>

 

