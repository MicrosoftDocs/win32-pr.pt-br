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
ms.openlocfilehash: 5bdbb854821f2a25565241700d28964b2d32319bccb8226c3d7d789c0e457fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094586"
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

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) é usado para determinar o valor de cor atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

