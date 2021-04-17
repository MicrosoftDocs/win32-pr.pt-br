---
title: Mensagem de WM_DWMCOMPOSITIONCHANGED (WinUser. h)
description: Informa todas as janelas de nível superior que a composição de Gerenciador de Janelas da Área de Trabalho (DWM) foi habilitada ou desabilitada.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Mensagem de WM_DWMCOMPOSITIONCHANGED Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763160"
---
# <a name="wm_dwmcompositionchanged-message"></a>Mensagem do WM \_ DWMCOMPOSITIONCHANGED

Informa todas as janelas de nível superior que a composição de Gerenciador de Janelas da Área de Trabalho (DWM) foi habilitada ou desabilitada.

> [!Note]  
> A partir do Windows 8, a composição do DWM é sempre habilitada, portanto, essa mensagem não é enviada independentemente das alterações no modo de vídeo.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

A função [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) pode ser usada para determinar o estado de composição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

