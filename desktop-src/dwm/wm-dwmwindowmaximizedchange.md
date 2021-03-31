---
title: Mensagem de WM_DWMWINDOWMAXIMIZEDCHANGE (WinUser. h)
description: Enviado quando uma janela composta de Gerenciador de Janelas da Área de Trabalho (DWM) é maximizada.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Mensagem de WM_DWMWINDOWMAXIMIZEDCHANGE Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369653"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>Mensagem do WM \_ DWMWINDOWMAXIMIZEDCHANGE

Enviado quando uma janela composta de Gerenciador de Janelas da Área de Trabalho (DWM) é maximizada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Defina como true para especificar que a janela foi maximizada.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

