---
title: PSN_KILLACTIVE código de notificação (Prsht. h)
description: Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão OK. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE de código de notificação controles do Windows
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
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918342"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

