---
title: PSN_TRANSLATEACCELERATOR código de notificação (Prsht. h)
description: Notifica uma folha de propriedades de que uma mensagem do teclado foi recebida. Ele fornece à página uma oportunidade de fazer a tradução do acelerador de teclado privado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811139"
---
# <a name="psn_translateaccelerator-notification-code"></a>\_Código de notificação PSN TRANSLATEACCELERATOR

Notifica uma folha de propriedades de que uma mensagem do teclado foi recebida. Ele fornece à página uma oportunidade de fazer a tradução do acelerador de teclado privado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** da estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** é um ponteiro para a [**msg**](/windows/win32/api/winuser/ns-winuser-msg)da mensagem. Ele pode ser convertido em um tipo **LPMSG** para obter acesso aos parâmetros da mensagem a ser traduzida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna PSNRET \_ MESSAGEHANDLED para indicar que nenhum processamento adicional é necessário. Retorna PSNRET \_ NOERROR para solicitar o processamento normal.

## <a name="remarks"></a>Comentários

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL. O procedimento da caixa de diálogo deve retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

