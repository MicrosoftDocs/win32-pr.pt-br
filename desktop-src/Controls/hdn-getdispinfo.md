---
title: HDN_GETDISPINFO de notificação (Commctrl.h)
description: Enviado ao proprietário de um controle de header quando o controle precisa de informações sobre um item de header de retorno de chamada. Esse código de notificação é enviado como uma mensagem WM \_ NOTIFY.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO código de notificação Windows Controles
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6e6cbc9559cda3312ecdca341aa7c7ad2b44dc5cc29e50690ddf10b2729a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435446"
---
# <a name="hdn_getdispinfo-notification-code"></a>Código de \_ notificação DO HDN GETDISPINFO

Enviado ao proprietário de um controle de header quando o controle precisa de informações sobre um item de header de retorno de chamada. Esse código de notificação é enviado como uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMHDDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) Na entrada, os campos da estrutura especificam quais informações são necessárias e o item de interesse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um LRESULT.

## <a name="remarks"></a>Comentários

Preencha os membros apropriados da estrutura para retornar as informações solicitadas para o controle de header. Se o manipulador  de mensagens definir o membro de máscara da estrutura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) como HDI \_ DI SETITEM, o controle de header armazenará as informações e não as solicitará \_ novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





