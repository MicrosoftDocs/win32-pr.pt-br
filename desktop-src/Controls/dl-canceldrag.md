---
title: DL_CANCELDRAG código de notificação (commctrl. h)
description: Sinaliza que o usuário cancelou uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086559"
---
# <a name="dl_canceldrag-notification-code"></a>Código de notificação do DL \_ CANCELDRAG

Sinaliza que o usuário cancelou uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o \_ código de notificação DL CANCELDRAG, o identificador para a caixa de listagem de arrastar e a posição do cursor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Ao processar o \_ código de notificação DL CANCELDRAG, um aplicativo pode redefinir seu estado interno para indicar que arrastar não está em vigor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





