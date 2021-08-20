---
title: CBEN_GETDISPINFO de notificação (Commctrl.h)
description: Enviado para recuperar informações de exibição sobre um item de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO de notificação Windows Controles
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896d282426c11f40fe949c73f44eb963a399c5c210e839198527f9bc903e2fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413689"
---
# <a name="cben_getdispinfo-notification-code"></a>Código de \_ notificação CBEN GETDISPINFO

Enviado para recuperar informações de exibição sobre um item de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que está processando esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

A [**estrutura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contém uma [**estrutura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) O **membro** mask especifica as informações que estão sendo solicitadas pelo controle .

Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle. Se o manipulador  de mensagens definir o membro de máscara da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) como CBEIF \_ DI SETITEM, o controle armazenará as informações e não as solicitará \_ novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEN \_ GETDISPINFOW** (Unicode) e **CBEN \_ GETDISPINFOA** (ANSI)<br/>         |



 

 





