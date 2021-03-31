---
title: Mensagem de TVM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetBkColor.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Controles de TVM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824513"
---
# <a name="tvm_setbkcolor-message"></a>\_Mensagem TVM SETBKCOLOR

Define a cor do plano de fundo do controle. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor do plano de fundo. Se esse valor for-1, o controle será revertido para usar a cor do sistema para a cor do plano de fundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor do plano de fundo anterior. Se esse valor for-1, o controle estava usando a cor do sistema para a cor do plano de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

