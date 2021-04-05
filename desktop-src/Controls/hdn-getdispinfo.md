---
title: HDN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado ao proprietário de um controle de cabeçalho quando o controle precisa de informações sobre um item de cabeçalho de retorno de chamada. Esse código de notificação é enviado como uma \_ mensagem de notificação do WM.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO de código de notificação controles do Windows
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
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008941"
---
# <a name="hdn_getdispinfo-notification-code"></a>Código de notificação do HDN \_ GETDISPINFO

Enviado ao proprietário de um controle de cabeçalho quando o controle precisa de informações sobre um item de cabeçalho de retorno de chamada. Esse código de notificação é enviado como uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) . Na entrada, os campos da estrutura especificam quais informações são necessárias e o item de interesse.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um LRESULT.

## <a name="remarks"></a>Comentários

Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle de cabeçalho. Se o manipulador de mensagens definir o membro **Mask** da estrutura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) para HDI \_ di \_ SETITEM, o controle de cabeçalho armazenará as informações e não a solicitará novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





