---
title: Mensagem de TVM_SETTEXTCOLOR (commctrl. h)
description: Define a cor do texto do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetTextColor.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Controles de TVM_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644774"
---
# <a name="tvm_settextcolor-message"></a>\_Mensagem TVM SETTEXTCOLOR

Define a cor do texto do controle. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor do texto. Se esse argumento for-1, o controle será revertido para usar a cor do sistema para a cor do texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **COLORREF** que representa a cor do texto anterior. Se esse valor for-1, o controle estava usando a cor do sistema para a cor do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

