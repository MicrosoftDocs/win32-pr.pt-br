---
title: PSN_HELP de notificação (Prsht.h)
description: Notifica uma página de que o usuário clicou no botão Ajuda. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP de notificação Windows Controles
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f03dc1e016780494c8c5ca35e62baf2570af04ee77daf21f404d7371e9df168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588196"
---
# <a name="psn_help-notification-code"></a>Código de notificação \_ do PSN HELP

Notifica uma página de que o usuário clicou no botão Ajuda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **hdr**. O **membro hwndFrom** dessa estrutura **NMHDR** contém o handle para a folha de propriedades. O **membro lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deve exibir informações de Ajuda para a página.

> [!Note]  
> Não há suporte para esse código de notificação ao usar o estilo do assistente do Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





