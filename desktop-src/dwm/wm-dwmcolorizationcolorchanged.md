---
title: Mensagem de WM_DWMCOLORIZATIONCOLORCHANGED (WinUser. h)
description: Informa todas as janelas de nível superior que a cor de colorização alterou.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Mensagem de WM_DWMCOLORIZATIONCOLORCHANGED Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085643"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>Mensagem do WM \_ DWMCOLORIZATIONCOLORCHANGED

Informa todas as janelas de nível superior que a cor de colorização alterou.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a nova cor de colorização. O formato de cor é 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica se a nova cor é mesclada com opacidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) é usado para determinar o valor de cor atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

