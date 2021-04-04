---
title: Mensagem de LVM_SETITEMTEXT (commctrl. h)
description: Altera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemText do ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Controles de LVM_SETITEMTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824454"
---
# <a name="lvm_setitemtext-message"></a>\_Mensagem SETITEMTEXT LVM

Altera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . O membro **iSubItem** é o índice do subitem ou pode ser zero para definir o rótulo do item. O membro **pszText** é o endereço de uma cadeia de caracteres terminada em nulo que contém o novo texto; Ele também pode ser **nulo**. O membro **pszText** também pode ser LPSTR \_ textcallback para indicar um item de retorno de chamada para o qual a janela pai armazena o texto. Nesse caso, o controle List-View envia ao pai um código de notificação [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) quando ele precisa do texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se você enviar essa mensagem explicitamente, ela retornará **true** se for bem-sucedida ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





