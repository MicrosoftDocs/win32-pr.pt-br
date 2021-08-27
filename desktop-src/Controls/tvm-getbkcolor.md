---
title: TVM_GETBKCOLOR mensagem (Commctrl.h)
description: Recupera a cor da tela de fundo atual do controle. Você pode enviar essa mensagem explicitamente ou usando a \_ macro TreeView GetBkColor.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a6530b1aada1fab06c0b353d7ead666e61f0f796b890d1f5c56fe0be094b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088446"
---
# <a name="tvm_getbkcolor-message"></a>Mensagem TVM \_ GETBKCOLOR

Recupera a cor da tela de fundo atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ TreeView GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa a cor da tela de fundo atual. Se esse valor for -1, o controle está usando a cor do sistema para a cor da tela de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

