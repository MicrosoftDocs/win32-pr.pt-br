---
title: TVM_GETITEMSTATE mensagem (Commctrl.h)
description: Recupera alguns ou todos os atributos de estado de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItemState.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE controles Windows mensagem
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
ms.openlocfilehash: ff562af5a97684caa3e5b17ab47d0f67f82a6789e2510cf1598a3189073fda81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261256"
---
# <a name="tvm_getitemstate-message"></a>Mensagem TVM \_ GETITEMSTATE

Recupera alguns ou todos os atributos de estado de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com o item.

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara usada para especificar os estados pelos quais consultar. É equivalente ao membro **stateMask** de [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor UINT** com os bits de estado apropriados definidos como **TRUE.** Somente os bits especificados por *lParam* e que são **TRUE** serão definidos. Esse valor é equivalente ao **membro de** estado [**de TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





