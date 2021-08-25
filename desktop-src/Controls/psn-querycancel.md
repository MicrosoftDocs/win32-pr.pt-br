---
title: PSN_QUERYCANCEL código de notificação (Prsht. h)
description: Indica que o usuário cancelou a folha de propriedades. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL código de notificação Windows controles
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff5ed6203d255a18c40044febb2f7afd9ab42e15c5a9d8ae9fa1a1a56518693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798616"
---
# <a name="psn_querycancel-notification-code"></a>Código de notificação do PSN \_ QUERYCANCEL

Indica que o usuário cancelou a folha de propriedades. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** para impedir a operação de cancelamento ou **false** para permiti-la.

## <a name="remarks"></a>Comentários

Esse código de notificação normalmente é enviado quando um usuário clica no botão **Cancelar** . Ele também é enviado quando um usuário clica no botão **X** no canto superior direito da folha de propriedades ou pressiona a tecla escape. Uma página de folha de propriedades pode manipular esse código de notificação para solicitar que o usuário Verifique a operação de cancelamento.

Para definir um valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT definido como o valor de retorno. O procedimento da caixa de diálogo deve retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

