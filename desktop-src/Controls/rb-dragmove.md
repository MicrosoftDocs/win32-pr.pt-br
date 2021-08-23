---
title: RB_DRAGMOVE mensagem (Commctrl.h)
description: Atualiza a posição de arrastar no controle de barra de rebar após uma mensagem BEGINDRAG do RB \_ anterior.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE controles Windows mensagem
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
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409718"
---
# <a name="rb_dragmove-message"></a>Mensagem \_ RB DRAGMOVE

Atualiza a posição de arrastar no controle de barra de rebar após uma mensagem [**\_ BEGINDRAG do RB**](rb-begindrag.md) anterior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor DWORD** que contém as novas coordenadas do mouse. A coordenada horizontal está contida no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e a coordenada vertical está contida no [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Se você passar (DWORD)-1, o controle de barra de rebar usará a posição do mouse na última vez que o thread do controle chamado [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 

