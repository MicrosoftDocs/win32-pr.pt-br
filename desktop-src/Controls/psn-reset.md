---
title: PSN_RESET de notificação (Prsht.h)
description: Notifica uma página de que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET código de notificação Windows Controles
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
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409806"
---
# <a name="psn_reset-notification-code"></a>Código de \_ notificação PSN RESET

Notifica uma página de que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Todas as alterações feitas desde o último código de notificação [PSN \_ APPLY](psn-apply.md) são canceladas, exceto no caso do [**PSH \_ AEROWIZARD,**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)que não dá suporte a esse código de notificação.

O **membro lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **TRUE** se o usuário clicou no **botão X** no canto superior direito da folha de propriedades. Será FALSE **se** o usuário clicou no **botão** Cancelar. A **estrutura PSHNOTIFY** contém uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **hdr**. O **membro hwndFrom** dessa estrutura **NMHDR** contém o handle para a folha de propriedades.

Um aplicativo pode usar esse código de notificação como uma oportunidade para executar operações de limpeza.

> [!Note]  
> A folha de propriedades está no processo de manipular a lista de páginas quando o código de notificação \_ PSN RESET é enviado. Não tente adicionar, remover ou inserir páginas ao manipular esse código de notificação. Isso terá resultados imprevisíveis.

 

Não chame a [**função EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar esse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

