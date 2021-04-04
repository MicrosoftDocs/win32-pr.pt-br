---
title: DL_BEGINDRAG código de notificação (commctrl. h)
description: Notifica a janela pai da caixa de listagem de arrastar que o usuário clicou com o botão esquerdo do mouse em um item. Uma caixa de listagem de arrastar envia esse código de notificação na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte arrastar mensagens da caixa de listagem.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824869"
---
# <a name="dl_begindrag-notification-code"></a>Código de notificação do DL \_ BEGINDRAG

Notifica a janela pai da caixa de listagem de arrastar que o usuário clicou com o botão esquerdo do mouse em um item. Uma caixa de listagem de arrastar envia esse código de notificação na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o \_ código de notificação DL BEGINDRAG, o identificador para a caixa de listagem de arrastar e a posição do cursor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne **true** para iniciar a operação de arrastar ou **false** para evitar a operação de arrastar.

## <a name="remarks"></a>Comentários

Ao processar esse código de notificação, um procedimento de janela normalmente determina o item de lista na posição do cursor especificado usando a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Em seguida, ele retorna **true** ou **false**, dependendo se o item deve ser arrastado. Antes de retornar **true**, o procedimento de janela deve salvar o índice do item de lista para que o aplicativo saiba qual item mover ou copiar quando a operação de arrastar for concluída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





