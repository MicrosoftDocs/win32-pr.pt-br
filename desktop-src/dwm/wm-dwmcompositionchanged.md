---
title: WM_DWMCOMPOSITIONCHANGED mensagem (Winuser.h)
description: Informa a todas as janelas de nível superior Gerenciador de Janelas da Área de Trabalho composição DWM foi habilitada ou desabilitada.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED mensagem Gerenciador de Janelas da Área de Trabalho
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
ms.openlocfilehash: 9973c69e114882041fc300ca6dee9c96efe121ee7bbf10875ed58ed3c269772c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118790"
---
# <a name="wm_dwmcompositionchanged-message"></a>Mensagem WM \_ DWMCOMPOSITIONCHANGED

Informa a todas as janelas de nível superior Gerenciador de Janelas da Área de Trabalho composição DWM foi habilitada ou desabilitada.

> [!Note]  
> A partir Windows 8, a composição DWM está sempre habilitada, portanto, essa mensagem não é enviada, independentemente das alterações no modo de vídeo.

 

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

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

A [**função DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) pode ser usada para determinar o estado de composição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

