---
title: PSN_APPLY código de notificação (Prsht. h)
description: Enviado a cada página na folha de propriedades para indicar que o usuário clicou no botão OK, fechar ou aplicar e quer que todas as alterações entrem em vigor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY de código de notificação controles do Windows
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
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455423"
---
# <a name="psn_apply-notification-code"></a>PSN \_ aplicar código de notificação

Enviado a cada página na folha de propriedades para indicar que o usuário clicou no botão OK, fechar ou aplicar e quer que todas as alterações entrem em vigor. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação, incluindo a ID da página.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Defina PSNRET \_ NOERROR para indicar que as alterações feitas nesta página são válidas e foram aplicadas. Se todas as páginas definirem PSNRET \_ NOERROR, a folha de propriedades poderá ser destruída. Para indicar que as alterações feitas nesta página são inválidas e para impedir que a folha de propriedades seja destruída, defina um dos seguintes valores de retorno:

-   PSNRET \_ inválido. A folha de propriedades não será destruída e o foco será retornado para esta página.
-   PSNRET \_ NOCHANGEPAGE inválida \_ . A folha de propriedades não será destruída e o foco será retornado para a página que tinha o foco quando o botão foi pressionado.

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.

## <a name="remarks"></a>Comentários

Quando o usuário clica no botão OK, aplicar ou fechar, a folha de propriedades envia uma notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página ativa, dando a ela uma oportunidade de validar as alterações do usuário. Se as alterações forem válidas, a folha de propriedades enviará um \_ código de notificação PSN aplicar a cada página, direcionando-a para aplicar as novas propriedades ao item correspondente.

> [!Note]  
> A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN aplicar é enviado. Não tente adicionar, remover ou inserir páginas enquanto manipula essa notificação. Isso terá resultados imprevisíveis.

 

O membro **lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **true** se o usuário clicar no botão OK. Ele também será definido como **true** se a mensagem de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) tiver sido enviada e o usuário clicar no botão fechar. Ele será definido como **false** se o usuário clicar no botão Aplicar.

A estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.

Não chame a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar este código de notificação.

Uma folha de propriedades modal é destruída se o usuário clica no botão OK e cada página retorna o \_ valor de NOERROR PSNRET em resposta a **PSN \_ Apply**. Se qualquer página retornar PSNRET \_ inválido ou PSNRET \_ \_ NOCHANGEPAGE inválido, o processo de aplicação será cancelado imediatamente. As páginas após a página de cancelamento não receberão um \_ código de notificação PSN aplicar.

Para receber esse código de notificação, uma página deve definir o \_ valor DWL MSGRESULT como **false** em resposta ao código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) .

> [!Note]  
> Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

