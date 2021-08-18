---
description: Notifica o sistema de que uma barra de aplicativos foi ativada. Uma barra de aplicativos deve chamar essa mensagem em resposta à mensagem WM \_ ACTIVATE.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224f04a88a1e69a1a67fc08c6018d33af2bcdbc6f34ff9fbd00d1dd76f82ce5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461129"
---
# <a name="abm_activate-message"></a>Mensagem DE ATIVAÇÃO do ABM \_

Notifica o sistema de que uma barra de aplicativos foi ativada. Uma barra de aplicativos deve chamar essa mensagem em resposta à [**mensagem WM \_ ACTIVATE.**](/windows/desktop/inputdev/wm-activate)


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma [**estrutura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica a barra de aplicativos a ser ativada. Você deve especificar os **membros cbSize** **e hWnd** ao enviar essa mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **TRUE.**

## <a name="remarks"></a>Comentários

Essa mensagem será ignorada se o **membro hWnd** da estrutura apontada por *pabd* identificar uma barra de aplicativos autohide. O sistema define automaticamente a ordem z para barras de aplicativo autohide.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

