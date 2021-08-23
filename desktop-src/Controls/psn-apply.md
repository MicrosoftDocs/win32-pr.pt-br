---
title: PSN_APPLY de notificação (Prsht.h)
description: Enviado para cada página na folha de propriedades para indicar que o usuário clicou no botão OK, Fechar ou Aplicar e deseja que todas as alterações entre em vigor. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY de notificação Windows Controles
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d4a0ea52f4cee495e689e8f0cdc91d7362ec3a1ee37ab81a911bc980d3209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410032"
---
# <a name="psn_apply-notification-code"></a>Código de \_ notificação PSN APPLY

Enviado para cada página na folha de propriedades para indicar que o usuário clicou no botão OK, Fechar ou Aplicar e deseja que todas as alterações entre em vigor. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação, incluindo a ID da página.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

De configurar PSNRET NOERROR para indicar que as alterações feitas nessa página são \_ válidas e foram aplicadas. Se todas as páginas definirem PSNRET \_ NOERROR, a folha de propriedades poderá ser destruída. Para indicar que as alterações feitas nessa página são inválidas e para impedir que a folha de propriedades seja destruída, de definido um dos seguintes valores de retorno:

-   PSNRET \_ INVÁLIDO. A folha de propriedades não será destruída e o foco será retornado para esta página.
-   PSNRET \_ \_ NOCHANGEPAGE INVÁLIDO. A folha de propriedades não será destruída e o foco será retornado para a página que tinha foco quando o botão foi pressionado.

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o valor MSGRESULT do DWL e o procedimento da caixa de diálogo deve retornar \_ **TRUE.**

## <a name="remarks"></a>Comentários

Quando o usuário clica no botão OK, Aplicar ou Fechar, a folha de propriedades envia uma notificação [ \_ KILLACTIVE PSN](psn-killactive.md) para a página ativa, dando a ele a oportunidade de validar as alterações do usuário. Se as alterações são válidas, a folha de propriedades envia um código de notificação PSN APPLY para cada página, direcionando-o para aplicar as novas propriedades \_ ao item correspondente.

> [!Note]  
> A folha de propriedades está no processo de manipular a lista de páginas quando o código de notificação \_ PSN APPLY é enviado. Não tente adicionar, remover ou inserir páginas durante a manipulação dessa notificação. Isso terá resultados imprevisíveis.

 

O **membro lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **TRUE** se o usuário clicar no botão OK. Ele também será definido como **TRUE** se a mensagem [**\_ CANCELTOCLOSE do PSM**](psm-canceltoclose.md) tiver sido enviada e o usuário clicar no botão Fechar. Ele será definido como **FALSE** se o usuário clicar no botão Aplicar.

A [**estrutura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contém uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **hdr**. O **membro hwndFrom** dessa estrutura **NMHDR** contém o handle para a folha de propriedades.

Não chame a [**função EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar esse código de notificação.

Uma folha de propriedades modais será destruída se o usuário clicar no botão OK e cada página retornar o valor PSNRET NOERROR em resposta a \_ **PSN \_ APPLY**. Se qualquer página retornar PSNRET \_ INVALID ou PSNRET \_ INVALID \_ NOCHANGEPAGE, o processo aplicar será cancelado imediatamente. As páginas após o cancelamento da página não receberão um código de notificação \_ PSN APPLY.

Para receber esse código de notificação, uma página deve definir o valor DWL MSGRESULT como FALSE em resposta ao código de notificação \_ [ \_ KILLACTIVE PSN.](psn-killactive.md) 

> [!Note]  
> Não há suporte para esse código de notificação ao usar o estilo do assistente do Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

