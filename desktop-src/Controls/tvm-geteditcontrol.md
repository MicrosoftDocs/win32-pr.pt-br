---
title: TVM_GETEDITCONTROL mensagem (Commctrl.h)
description: Recupera o alça para o controle de edição que está sendo usado para editar o texto de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetEditControl.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL controles de Windows mensagem
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
ms.openlocfilehash: a591104085de793d8ea479656eb9100424ba5194a173fd93d10444c43e2cbfc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104426"
---
# <a name="tvm_geteditcontrol-message"></a>Mensagem TVM \_ GETEDITCONTROL

Recupera o alça para o controle de edição que está sendo usado para editar o texto de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetEditControl.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para o controle de edição se for bem-sucedido ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Quando a edição de rótulo é iniciada, um controle de edição é criado, mas não posicionado ou exibido. Antes de ser exibido, o controle de exibição de árvore envia à janela pai um código de notificação [TVN \_ BEGINLABELEDIT.](tvn-beginlabeledit.md)

Para personalizar a edição de rótulo, implemente um manipulador [para TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) e envie uma mensagem **TVM \_ GETEDITCONTROL** para o controle de exibição de árvore. Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição. Use esse alça para personalizar o controle de edição enviando as mensagens **EM \_ XXX** usuais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





