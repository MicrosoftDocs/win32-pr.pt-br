---
title: Mensagem de LVM_GETEDITCONTROL (commctrl. h)
description: Obtém o identificador para o controle de edição usado para editar o texto de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetEditControl do ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Controles de LVM_GETEDITCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008865"
---
# <a name="lvm_geteditcontrol-message"></a>\_Mensagem GETEDITCONTROL LVM

Obtém o identificador para o controle de edição usado para editar o texto de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetEditControl do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de edição, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando o rótulo é iniciado, um controle de edição é criado, posicionado e inicializado. Antes de ser exibida, o controle List-View envia à janela pai um código de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .

Para personalizar a edição de rótulo, implemente um manipulador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e envie uma mensagem de **\_ GETEDITCONTROL LVM** para o controle de exibição de lista. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido. Você pode subclassear o controle de edição, mas não deve destruí-lo. Para cancelar a edição, envie o controle de exibição de lista para uma mensagem do [**WM \_ cancelable**](/windows/desktop/winmsg/wm-cancelmode) .

O item de exibição de lista que está sendo editado é o item atualmente focalizado, que é o item no estado focalizado. Para localizar um item com base em seu estado, use a mensagem [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetEditControl de ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

