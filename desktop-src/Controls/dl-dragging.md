---
title: DL_DRAGGING código de notificação (commctrl. h)
description: Sinaliza que o usuário moveu o mouse ao arrastar um item.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499870"
---
# <a name="dl_dragging-notification-code"></a>Código de notificação de arrastar para DL \_

Sinaliza que o usuário moveu o mouse ao arrastar um item. \_O recurso de DL também é enviado periodicamente durante a arrastar, mesmo que o mouse não seja movido. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador de controle da caixa de listagem de arrastar.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o código de notificação de arrastar da DL \_ , o identificador para a caixa de listagem de arrastar e a posição do cursor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno determina o tipo de cursor do mouse que a lista de arrastar deve definir; pode ser o valor DL \_ STOPCURSOR, DL \_ COPYCURSOR ou DL \_ MOVECURSOR. Se qualquer outro valor for retornado, o cursor não será alterado.

## <a name="remarks"></a>Comentários

Um procedimento de janela normalmente processa o \_ código de notificação de arrastar da DL determinando o item sob o cursor e, em seguida, desenhando um ícone de inserção. Para recuperar o item sob o cursor, use a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , especificando **true** para o parâmetro *bAutoScroll* . Essa opção faz com que a caixa de listagem de arrastar role periodicamente se o cursor estiver acima ou abaixo da área do cliente. Para desenhar o ícone de inserção, use a função [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





