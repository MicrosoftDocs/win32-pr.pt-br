---
title: Mensagem de TVM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Controles de TVM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824266"
---
# <a name="tvm_insertitem-message"></a>\_Mensagem TVM INSERTITEM

Insere um novo item em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica os atributos do item de exibição de árvore.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador **HTREEITEM** para o novo item, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) e **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





