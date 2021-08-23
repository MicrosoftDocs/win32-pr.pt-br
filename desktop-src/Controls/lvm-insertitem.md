---
title: LVM_INSERTITEM mensagem (Commctrl.h)
description: Insere um novo item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertItem ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9408a8d09adca2a097281b13e56241c66a68521dcef0892502d7f8d0e14d25e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575706"
---
# <a name="lvm_insertitem-message"></a>Mensagem LVM \_ INSERTITEM

Insere um novo item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertItem ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica os atributos do item de exibição de lista. Use o **membro iItem** para especificar o índice baseado em zero no qual o novo item deve ser inserido. Se esse valor for maior que o número de itens atualmente contidos pela listview, o novo item será anexado ao final da lista e atribuído ao índice correto. Examine o valor de retorno da mensagem para determinar o índice real atribuído ao item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do novo item se for bem-sucedido ou -1 caso contrário.

## <a name="remarks"></a>Comentários

Não é possível usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou **LVM \_ INSERTITEM** para inserir subitens. O **membro iSubItem** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve ser zero. Consulte [**LVM \_ SETITEM para**](lvm-setitem.md) obter informações sobre como definir subitens.

Se um controle de exibição de lista tiver o estilo [**\_ \_ CHECKBOXES LVS EX**](extended-list-view-styles.md) definido, qualquer valor colocado nos bits 12 a 15 do membro de estado da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) será ignorado.  Quando um item é adicionado com esse conjunto de estilos, ele sempre será definido como o estado desmarcado.

Se um controle de exibição de lista tiver o estilo de janela [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING,**](list-view-window-styles.md) uma mensagem **LVM \_ INSERTITEM** falhará se você tentar inserir um item que tenha LPSTR TEXTCALLBACK como o valor de seu membro \_ **pszText.**

A **mensagem LVM \_ INSERTITEM** inserirá o novo item na posição adequada na ordem de classificação se as seguintes condições se manterem:

-   Você está usando um dos estilos \_ SORTXXX LVS.
-   Você não está usando o [**estilo LVS \_ OWNERDRAW.**](list-view-window-styles.md)
-   O **membro pszText** da estrutura apontada por **pitem** não está definido como LPSTR \_ TEXTCALLBACK.

Se a [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) não contém LVIF GROUPID no membro de máscara, o valor do membro \_ **iGroupId** é I  \_ GROUPIDCALLBACK por padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





