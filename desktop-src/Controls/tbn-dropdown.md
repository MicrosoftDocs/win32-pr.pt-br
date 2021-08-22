---
title: TBN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um botão suspenso. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN código de notificação Windows controles
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2cdee38176b2ed72d42aaa29ca685a5e73dd30ceb7e315b5cbe0971161dc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077920"
---
# <a name="tbn_dropdown-notification-code"></a>\_Código de notificação da lista suspensa tbn

Enviado por um controle Toolbar quando o usuário clica em um botão suspenso. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre este código de notificação. Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores:



| Código de retorno                                                                                          | Descrição                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ padrão**</dt> </dl>      | A lista suspensa foi tratada.<br/>                                             |
| <dl> <dt>**TBDDRET \_ padrão**</dt> </dl>    | A lista suspensa não foi tratada.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | A lista suspensa foi tratada, mas trata o botão como um botão normal.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Os botões suspensos podem ser simples (estilo de [**\_ lista suspensa BTNS**](toolbar-control-and-button-styles.md) ), exibir uma seta ao lado da imagem do botão (estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) ) ou exibir uma seta que é separada do estilo da imagem ([**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ). Se uma seta separada for usada, \_ a lista suspensa tbn será enviada somente se o usuário clicar na parte de seta do botão. Se o usuário clicar na parte principal do botão, uma mensagem [**de \_ comando do WM**](/windows/desktop/menurc/wm-command) com a ID do botão será enviada, assim como com um botão padrão. Para os outros dois estilos de botão suspenso, a \_ lista suspensa tbn é enviada quando o usuário clica em qualquer parte do botão.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

