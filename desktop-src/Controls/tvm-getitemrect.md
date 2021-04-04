---
title: Mensagem de TVM_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador para um item de exibição de árvore e indica se o item está visível. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItemRect.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Controles de TVM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085454"
---
# <a name="tvm_getitemrect-message"></a>\_Mensagem TVM GETITEMRECT

Recupera o retângulo delimitador para um item de exibição de árvore e indica se o item está visível. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica a parte do item para o qual recuperar o retângulo delimitador. Se esse parâmetro for **true**, o retângulo delimitador incluirá apenas o texto do item. Caso contrário, inclui a linha inteira que o item ocupa no controle de exibição em árvore.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que, ao enviar a mensagem, contém o identificador do item para o qual recuperar o retângulo. Consulte o exemplo abaixo para obter mais informações sobre como posicionar o identificador de item nesse parâmetro. Depois de retornar da mensagem, esse parâmetro contém o retângulo delimitador. As coordenadas são relativas ao canto superior esquerdo do controle de exibição de árvore.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o item estiver visível e o retângulo delimitador for recuperado com êxito, o valor de retorno será **true**. Caso contrário, a mensagem retornará **false** e não recuperará o retângulo delimitador.

## <a name="remarks"></a>Comentários

Ao enviar essa mensagem, o parâmetro *lParam* contém o identificador do item para o qual o retângulo está sendo recuperado. O identificador é colocado em *lParam* , conforme mostrado no exemplo a seguir:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

