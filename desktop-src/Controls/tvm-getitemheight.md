---
title: Mensagem de TVM_GETITEMHEIGHT (commctrl. h)
description: Recupera a altura atual de cada item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItemHeight.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Controles de TVM_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824839"
---
# <a name="tvm_getitemheight-message"></a>\_Mensagem TVM GETITEMHEIGHT

Recupera a altura atual de cada item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a altura de cada item, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETITEMHEIGHT**](tvm-setitemheight.md)
</dt> </dl>

 

 





