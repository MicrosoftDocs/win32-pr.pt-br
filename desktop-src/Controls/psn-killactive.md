---
title: PSN_KILLACTIVE código de notificação (Prsht. h)
description: Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão OK. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE código de notificação Windows controles
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eaf1a5221e186ebe5f01f942ec99d82906ea87ef7f1b8f73860bade24ab1751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169646"
---
# <a name="psn_killactive-notification-code"></a>Código de notificação do PSN \_ KILLACTIVE

Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão OK. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades. O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** para impedir que a página perca a ativação ou **false** para permiti-la.

## <a name="remarks"></a>Comentários

Um aplicativo manipula esse código de notificação para validar as informações inseridas pelo usuário.

> [!Note]  
> A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN KILLACTIVE é enviado. Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação. Isso terá resultados imprevisíveis.

 

Para definir um valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com um \_ valor DWL MSGRESULT definido como o valor de retorno. O procedimento da caixa de diálogo deve retornar **true**.

Se o procedimento da caixa de diálogo Definir DWL \_ MSGRESULT como **true**, ele deverá exibir uma caixa de mensagem para explicar o problema ao usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

