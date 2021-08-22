---
title: PSN_WIZFINISH de notificação (Prsht.h)
description: Notifica uma página de que o usuário clicou no botão Concluir em um assistente. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH código de notificação Windows Controles
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
ms.openlocfilehash: b9a11b018a57126c0882862271fa209fcd507224a46180ebb5fbaed4355fc040
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588176"
---
# <a name="psn_wizfinish-notification-code"></a>Código de notificação \_ WIZFINISH PSN

Notifica uma página de que o usuário clicou no **botão** Concluir em um assistente. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação. Essa estrutura contém uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **hdr**. O **membro hwndFrom** dessa estrutura **NMHDR** contém o handle para a folha de propriedades. O **membro lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

-   Retorna **TRUE para** impedir que o assistente seja finalizando.
-   [Versão 5.80.](common-control-versions.md) e posterior. Retorna um alça de janela para impedir que o assistente seja finalizando. O assistente definirá o foco para essa janela. A janela deve ser de propriedade da página do assistente.
-   Retorna **FALSE** para permitir que o assistente seja finalado.

## <a name="remarks"></a>Comentários

Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o valor MSGRESULT do DWL e o procedimento da caixa de diálogo deve retornar \_ **TRUE.**

[Versão 5.80.](common-control-versions.md) Se o aplicativo retornar **TRUE para** impedir que um assistente seja final, ele não terá controle sobre qual janela na página recebe o foco. Os aplicativos que precisam interromper a conclusão de um assistente normalmente devem fazer isso retornando o alça da janela na página do assistente que deve receber o foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

