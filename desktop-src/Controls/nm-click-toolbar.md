---
title: Código de notificação de NM_CLICK (barra de ferramentas) (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Código de notificação de NM_CLICK (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824853"
---
# <a name="nm_click-toolbar-notification-code"></a>\_Código de notificação de clique do nm (barra de ferramentas)

Enviado por um controle Toolbar quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação. O membro **dwItemSpec** contém o índice da seção que foi clicada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true** para indicar que o clique do mouse foi tratado e suprimir o processamento padrão pelo sistema. Retorne **false** para permitir o processamento padrão do clique.

## <a name="remarks"></a>Comentários

Clicar em um item com o botão esquerdo do mouse faz com que a barra de ferramentas envie uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) com o código de notificação [ \_ clicado bilhão](bn-clicked.md) para a janela pai. A notificação de clique de NM \_ é enviada após a mensagem de **\_ comando do WM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

