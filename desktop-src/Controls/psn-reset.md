---
title: PSN_RESET código de notificação (Prsht. h)
description: Notifica uma página que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748254"
---
# <a name="psn_reset-notification-code"></a>\_Código de notificação de redefinição de PSN

Notifica uma página que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Todas as alterações feitas desde o último código de notificação de [ \_ aplicação de PSN](psn-apply.md) são canceladas, exceto no caso de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), que não oferece suporte a esse código de notificação.

O membro **lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **true** se o usuário clicar no botão **X** no canto superior direito da folha de propriedades. Será **false** se o usuário clicou no botão **Cancelar** . A estrutura **PSHNOTIFY** contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.

Um aplicativo pode usar esse código de notificação como uma oportunidade para executar operações de limpeza.

> [!Note]  
> A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação de redefinição de PSN é enviado. Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação. Isso terá resultados imprevisíveis.

 

Não chame a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar este código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

