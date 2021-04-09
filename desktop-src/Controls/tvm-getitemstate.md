---
title: Mensagem de TVM_GETITEMSTATE (commctrl. h)
description: Recupera alguns ou todos os atributos de estado de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemState do TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Controles de TVM_GETITEMSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009548"
---
# <a name="tvm_getitemstate-message"></a>\_Mensagem TVM GETitemstate

Recupera alguns ou todos os atributos de estado de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemState do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o item.

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara usada para especificar os Estados a serem consultados. É equivalente ao membro **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **uint** com os bits de estado apropriados definidos como **true**. Somente os bits especificados por *lParam* e que são **true** serão definidos. Esse valor é equivalente ao **estado** membro de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





