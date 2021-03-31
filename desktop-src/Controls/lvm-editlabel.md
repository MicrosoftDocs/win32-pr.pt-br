---
title: Mensagem de LVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item de exibição de lista especificado. A mensagem seleciona implicitamente e concentra o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro EditLabel do ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Controles de LVM_EDITLABEL de mensagens do Windows
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
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644266"
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

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de edição que é usado para editar o texto do item, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido. Você pode subclassear o controle de edição, mas não deve destruí-lo.

O controle deve ter o foco antes de você enviar esta mensagem para o controle. O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

Se *wParam* for-1, um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) será enviado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**cancelamento do WM \_**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

