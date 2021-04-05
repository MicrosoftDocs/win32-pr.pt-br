---
title: HDN_ITEMCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824683"
---
# <a name="hdn_itemclick-notification-code"></a>Código de notificação do HDN \_ DOclick

Notifica uma janela pai do controle de cabeçalho que o usuário clicou no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que identifica o controle de cabeçalho e especifica o índice do item de cabeçalho que foi clicado e o botão do mouse usado para clicar no item. O membro **pItem** está definido como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um controle de cabeçalho envia esse código de notificação depois que o usuário libera o botão esquerdo do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) e **HDN ao \_ clicar** (ANSI)<br/>               |



 

 





