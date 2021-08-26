---
title: TVM_GETITEMRECT mensagem (Commctrl.h)
description: Recupera o retângulo delimitado para um item de exibição de árvore e indica se o item está visível. Você pode enviar essa mensagem explicitamente ou usando a \_ macro TreeView GetItemRect.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT controles de Windows mensagem
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
ms.openlocfilehash: 1c6b58ff7d2ce88fd4257ce7db84fa8bd9b4fa2b2d223af03a3f1d57a83c9b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053996"
---
# <a name="tvm_getitemrect-message"></a>Mensagem TVM \_ GETITEMRECT

Recupera o retângulo delimitado para um item de exibição de árvore e indica se o item está visível. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ TreeView GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica a parte do item para o qual recuperar o retângulo delimitado. Se esse parâmetro for **TRUE,** o retângulo delimitado incluirá apenas o texto do item. Caso contrário, ele incluirá toda a linha que o item ocupa no controle de exibição de árvore.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) para a que, ao enviar a mensagem, contém o alça do item para o que recuperar o retângulo. Consulte o exemplo abaixo para obter mais informações sobre como colocar o alça de item nesse parâmetro. Depois de retornar da mensagem, esse parâmetro conterá o retângulo delimitado. As coordenadas são relativas ao canto superior esquerdo do controle de exibição de árvore.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o item estiver visível e o retângulo delimitativo tiver sido recuperado com êxito, o valor de retorno será **TRUE.** Caso contrário, a mensagem **retornará FALSE** e não recuperará o retângulo delimitado.

## <a name="remarks"></a>Comentários

Ao enviar essa mensagem, o *parâmetro lParam* contém o alça do item para o que o retângulo está sendo recuperado. O handle é colocado em *lParam,* conforme mostrado no exemplo a seguir:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

