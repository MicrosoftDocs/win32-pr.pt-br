---
description: Notifica o sistema quando a posição de uma barra de aplicativos é alterada. Uma barra de aplicativos deve chamar essa mensagem em resposta à mensagem WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d770d50629342095308376856b98e6250adc1f9a1f2559da8509d685995428ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057806"
---
# <a name="abm_windowposchanged-message"></a>MENSAGEM ABM \_ WINDOWPOSCHANGED

Notifica o sistema quando a posição de uma barra de aplicativos é alterada. Uma barra de aplicativos deve chamar essa mensagem em resposta à mensagem [**WM \_ WINDOWPOSCHANGED.**](/windows/desktop/winmsg/wm-windowposchanged)


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
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

Essa mensagem será ignorada se o **membro hWnd** da estrutura apontada por *pabd* identificar uma barra de aplicativos autohide.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

