---
title: Mensagem de LVM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertItem do ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Controles de LVM_INSERTITEM de mensagens do Windows
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
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753965"
---
# <a name="lvm_insertitem-message"></a>\_Mensagem INSERTITEM LVM

Insere um novo item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica os atributos do item de exibição de lista. Use o membro **iItem** para especificar o índice de base zero no qual o novo item deve ser inserido. Se esse valor for maior que o número de itens contidos atualmente por ListView, o novo item será anexado ao final da lista e atribuído ao índice correto. Examine o valor de retorno da mensagem para determinar o índice real atribuído ao item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do novo item se for bem-sucedido ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Você não pode usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou **LVM \_ InsertItem** para inserir subitens. O membro **iSubItem** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve ser zero. Consulte [**LVM \_ SETITEM**](lvm-setitem.md) para obter informações sobre como configurar subitens.

Se um controle de exibição de lista tiver o estilo de [**\_ caixas de \_ seleção LVS ex**](extended-list-view-styles.md) definido, qualquer valor colocado em bits 12 a 15 do membro de **estado** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) será ignorado. Quando um item é adicionado com esse conjunto de estilos, ele sempre será definido como o estado desmarcado.

Se um controle de exibição de lista tiver o estilo de janela [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , uma mensagem do **LVM \_ INSERTITEM** falhará se você tentar inserir um item que tenha o do LPSTR \_ como o valor de seu membro **pszText** .

A mensagem **LVM \_ INSERTITEM** irá inserir o novo item na posição apropriada na ordem de classificação se as seguintes condições tiverem:

-   Você está usando um dos estilos LVS \_ SORTXXX.
-   Você não está usando o estilo [**LVS \_ OWNERDRAW**](list-view-window-styles.md) .
-   O membro **pszText** da estrutura apontada por **pItem** não está definido como \_ monocallback de LPSTR.

Se a estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) não contiver LVIF \_ GroupId no membro **Mask** , o valor do membro **iGroupId** será \_ GROUPIDCALLBACK por padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





