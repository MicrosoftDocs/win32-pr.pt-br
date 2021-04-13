---
title: LVN_COLUMNOVERFLOWCLICK código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o botão de estouro é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456055"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>Código de notificação do LVN \_ COLUMNOVERFLOWCLICK

Enviado por um controle de exibição de lista quando o botão de estouro é clicado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que descreve o código de notificação. O chamador é responsável por alocar essa estrutura, incluindo a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida. Defina os membros da estrutura **NMHDR** . O membro do **código** deve ser definido como LVN \_ COLUMNOVERFLOWCLICK.

Defina o membro **iItem** da estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) como-1. Defina o membro **iSubItem** para o índice do subitem. Defina os membros **uNewState**, **uOldState** e **lParam** como zero. Os membros restantes da estrutura **NMLISTVEIW** não são usados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . O parâmetro *wParam* contém a ID do controle que envia o código de notificação.

Se um controle de cabeçalho for um filho de ListView, o controle de cabeçalho deverá enviar esse código de notificação ao controle ListView quando o controle de cabeçalho receber o código de notificação [HDN \_ OVERFLOWCLICK](hdn-overflowclick.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





