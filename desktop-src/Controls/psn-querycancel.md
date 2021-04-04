---
title: PSN_QUERYCANCEL código de notificação (Prsht. h)
description: Indica que o usuário cancelou a folha de propriedades. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL de código de notificação controles do Windows
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
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918340"
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

## <a name="return-value"></a>Retornar valor

Retorna **true** para impedir a operação de cancelamento ou **false** para permiti-la.

## <a name="remarks"></a>Comentários

Esse código de notificação normalmente é enviado quando um usuário clica no botão **Cancelar** . Ele também é enviado quando um usuário clica no botão **X** no canto superior direito da folha de propriedades ou pressiona a tecla escape. Uma página de folha de propriedades pode manipular esse código de notificação para solicitar que o usuário Verifique a operação de cancelamento.

Para definir um valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT definido como o valor de retorno. O procedimento da caixa de diálogo deve retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

