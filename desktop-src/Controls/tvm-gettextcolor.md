---
title: Mensagem de TVM_GETTEXTCOLOR (commctrl. h)
description: Recupera a cor do texto atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetTextColor.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- controles de Windows de mensagem de TVM_GETTEXTCOLOR
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a578753b6f86d2ceaa6a664fe6e6e0ff88475dccfb953ae6c6f652bc2dffbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669707"
---
# <a name="tvm_gettextcolor-message"></a>\_Mensagem TVM GETTEXTCOLOR

Recupera a cor do texto atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor do texto atual. Se esse valor for-1, o controle estará usando a cor do sistema para a cor do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

