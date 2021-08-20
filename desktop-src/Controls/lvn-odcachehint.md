---
title: LVN_ODCACHEHINT código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista virtual quando o conteúdo de sua área de exibição foi alterado.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT código de notificação Windows controles
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3693291eeaef0879bdf861f392b89a1d0f2d5ec52f8a9c0d092b5495eb4565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170173"
---
# <a name="lvn_odcachehint-notification-code"></a>Código de notificação do LVN \_ ODCACHEHINT

Enviado por um controle de exibição de lista virtual quando o conteúdo de sua área de exibição foi alterado. Por exemplo, um controle de exibição de lista envia esse código de notificação quando o usuário rola a exibição do controle. O \_ código de notificação LVN ODCACHEHINT é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) que contém informações sobre o intervalo de itens a serem armazenados em cache.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que recebe esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Manipular essa mensagem permite que o aplicativo atualize as informações do item mantidas no cache para que ele esteja prontamente disponível quando um código de notificação [LVN \_ GETDISPINFO](lvn-getdispinfo.md) é enviado.

Observe que esse código de notificação nem sempre é uma representação exata dos itens que serão solicitados por [LVN \_ GETDISPINFO](lvn-getdispinfo.md). Portanto, se o item solicitado não for armazenado em cache durante o tratamento de LVN \_ GETDISPINFO, o aplicativo deverá estar preparado para fornecer as informações solicitadas de uma fonte fora do cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





