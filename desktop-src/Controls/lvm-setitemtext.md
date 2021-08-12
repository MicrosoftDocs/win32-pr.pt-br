---
title: LVM_SETITEMTEXT mensagem (Commctrl.h)
description: Altera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT controles de Windows mensagem
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
ms.openlocfilehash: 14eb5ddcff18a84f93febb22ef6661d8871df9b5578cc79f071b6e51b557c87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670869"
---
# <a name="lvm_setitemtext-message"></a>Mensagem LVM \_ SETITEMTEXT

Altera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a [**macro ListView \_ SetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) O **membro iSubItem** é o índice do subitem ou pode ser zero para definir o rótulo do item. O **membro pszText** é o endereço de uma cadeia de caracteres terminada em nulo que contém o novo texto; também pode ser **NULL.** O **membro pszText** também pode ser LPSTR TEXTCALLBACK para indicar um item de retorno de chamada para o qual a janela pai \_ armazena o texto. Nesse caso, o controle de exibição de lista envia ao pai um código de notificação [**\_ GETDISPINFO LVN**](lvn-getdispinfo.md) quando ele precisa do texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se você enviar essa mensagem explicitamente, ela retornará **TRUE se** for bem-sucedido ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





