---
title: Mensagem de TVM_GETEDITCONTROL (commctrl. h)
description: Recupera o identificador para o controle de edição usado para editar um texto do item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetEditControl.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Controles de TVM_GETEDITCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086316"
---
# <a name="tvm_geteditcontrol-message"></a>\_Mensagem TVM GETEDITCONTROL

Recupera o identificador para o controle de edição usado para editar um texto do item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de edição, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando o rótulo é iniciado, um controle de edição é criado, mas não posicionado ou exibido. Antes de ser exibida, o controle de exibição de árvore envia a janela pai um código de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .

Para personalizar a edição de rótulo, implemente um manipulador para [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) e envie uma mensagem **TVM \_ GETEDITCONTROL** para o controle de exibição em árvore. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





