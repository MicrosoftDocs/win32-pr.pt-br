---
title: WM_DWMNCRENDERINGCHANGED mensagem (Winuser.h)
description: Enviado quando a política de renderização de área não cliente foi alterada.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED mensagem Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcae8595315d43737d88d6a302bcac3a328418abd19d77b96bd13ee5ef66496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502649"
---
# <a name="wm_dwmncrenderingchanged-message"></a>Mensagem WM \_ DWMNCRENDERINGCHANGED

Enviado quando a política de renderização de área não cliente foi alterada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a renderização DWM está habilitada para a área não cliente da janela. **TRUE** se habilitado; caso contrário, **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

As [**funções DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) são usadas para obter ou definir a política de renderização não cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

