---
title: Mensagem de LVM_GETITEMTEXT (commctrl. h)
description: Recupera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemText do ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Controles de LVM_GETITEMTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086163"
---
# <a name="lvm_getitemtext-message"></a>\_Mensagem GETITEMTEXT LVM

Recupera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Para recuperar o texto do item, defina **iSubItem** como zero. Para recuperar o texto de um subitem, defina **iSubItem** como o índice do subitem. O membro **pszText** aponta para um buffer que recebe o texto. O membro **cchTextMax** especifica o número de caracteres no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se você enviar essa mensagem explicitamente, ela retornará o número de caracteres no membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="remarks"></a>Comentários

Você também pode enviar essa mensagem chamando a macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . No entanto, essa macro não retorna o comprimento da cadeia de caracteres.

**LVM \_** Não há suporte para GETITEMTEXT no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) e **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





