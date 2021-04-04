---
title: Código de notificação de NM_KEYDOWN (barra de ferramentas) (commctrl. h)
description: Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Código de notificação de NM_KEYDOWN (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008854"
---
# <a name="nm_keydown-toolbar-notification-code"></a>\_Código de notificação do nm KEYDOWN (Toolbar)

Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contém informações adicionais sobre a chave que causou o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar diferente de zero para impedir que o controle processe a chave ou zero caso contrário.

## <a name="remarks"></a>Comentários

Atualmente, somente o controle Toolbar envia esse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





