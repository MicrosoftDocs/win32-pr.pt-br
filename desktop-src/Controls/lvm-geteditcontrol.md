---
title: LVM_GETEDITCONTROL mensagem (Commctrl.h)
description: Obtém o controle de edição que está sendo usado para editar o texto de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ GetEditControl.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL controles de Windows mensagem
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
ms.openlocfilehash: 29f7e7ac31b3d429ab32ac6564a47f859f0e5dc2207d991cb580173838a4c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968306"
---
# <a name="lvm_geteditcontrol-message"></a>Mensagem GETEDITCONTROL do LVM \_

Obtém o controle de edição que está sendo usado para editar o texto de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**ListView \_ GetEditControl.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para o controle de edição se for bem-sucedido ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando a edição de rótulo é iniciada, um controle de edição é criado, posicionado e inicializado. Antes de ser exibido, o controle de exibição de lista envia à janela pai um código de notificação [LVN \_ BEGINLABELEDIT.](lvn-beginlabeledit.md)

Para personalizar a edição de rótulo, implemente um manipulador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e envie uma mensagem **\_ GETEDITCONTROL LVM** para o controle de exibição de lista. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse alça para personalizar o controle de edição enviando as mensagens **EM \_ XXX** usuais.

Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o handle não é mais válido. Você pode subclasse do controle de edição, mas não deve destruir. Para cancelar a edição, envie ao controle de exibição de lista uma [**mensagem WM \_ CANCELMODE.**](/windows/desktop/winmsg/wm-cancelmode)

O item de exibição de lista que está sendo editado é o item focalizado no momento, ou seja, o item no estado focalizado. Para encontrar um item com base em seu estado, use a [**mensagem \_ GETNEXTITEM LVM.**](lvm-getnextitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

