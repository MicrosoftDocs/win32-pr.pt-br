---
title: Mensagem de LVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item de exibição de lista especificado. A mensagem seleciona implicitamente e concentra o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro EditLabel do ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- controles de Windows de mensagem de LVM_EDITLABEL
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411840"
---
# <a name="lvm_editlabel-message"></a>\_Mensagem EDITLABEL LVM

Inicia a edição in-loco do texto do item de exibição de lista especificado. A mensagem seleciona implicitamente e concentra o item especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ EditLabel do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item de exibição de lista. Para cancelar a edição, defina o índice como-1.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para o controle de edição que é usado para editar o texto do item, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido. Você pode subclassear o controle de edição, mas não deve destruí-lo.

O controle deve ter o foco antes de você enviar esta mensagem para o controle. O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

Se *wParam* for-1, um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) será enviado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**cancelamento do WM \_**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

