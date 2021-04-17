---
title: Mensagem de TVM_GETBKCOLOR (commctrl. h)
description: Recupera a cor do plano de fundo atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetBkColor.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Controles de TVM_GETBKCOLOR de mensagens do Windows
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
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748251"
---
# <a name="tvm_getbkcolor-message"></a>\_Mensagem TVM GETBKCOLOR

Recupera a cor do plano de fundo atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de plano de fundo atual. Se esse valor for-1, o controle estará usando a cor do sistema para a cor do plano de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

