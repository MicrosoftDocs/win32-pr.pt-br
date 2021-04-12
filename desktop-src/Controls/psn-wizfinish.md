---
title: PSN_WIZFINISH código de notificação (Prsht. h)
description: Notifica uma página que o usuário clicou no botão concluir em um assistente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455538"
---
# <a name="psn_wizfinish-notification-code"></a>Código de notificação do PSN \_ WIZFINISH

Notifica uma página que o usuário clicou no botão **concluir** em um assistente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

-   Retorna **true** para impedir que o assistente seja concluído.
-   [Versão 5,80.](common-control-versions.md) e posterior. Retorna um identificador de janela para impedir que o assistente seja concluído. O assistente definirá o foco para essa janela. A janela deve pertencer à página do assistente.
-   Retorna **false** para permitir que o assistente seja concluído.

## <a name="remarks"></a>Comentários

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.

[Versão 5,80.](common-control-versions.md) Se seu aplicativo retornar **true** para impedir que um assistente seja concluído, ele não terá controle sobre qual janela na página recebe o foco. Os aplicativos que precisam parar a conclusão de um assistente normalmente devem fazer isso retornando o identificador da janela na página do assistente que deve receber o foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

