---
title: Mensagem de TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMarkColor.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Controles de TVM_SETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085721"
---
# <a name="tvm_setinsertmarkcolor-message"></a>\_Mensagem TVM SETINSERTMARKCOLOR

Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor de marca de inserção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **COLORREF** que contém a cor de marca de inserção anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

