---
description: Notifica o sistema de que um AppBar foi ativado. Um AppBar deve chamar essa mensagem em resposta à mensagem de \_ ativação do WM.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Mensagem de ABM_ACTIVATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090037"
---
# <a name="abm_activate-message"></a>ABM \_ Ativar mensagem

Notifica o sistema de que um AppBar foi ativado. Um AppBar deve chamar essa mensagem em resposta à mensagem [**de \_ ativação do WM**](/windows/desktop/inputdev/wm-activate) .


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica o AppBar a ser ativado. Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa mensagem será ignorada se o membro **HWND** da estrutura apontado por *pabd* identificar uma AutoOcultar AppBar. O sistema define automaticamente a ordem z para o AutoOcultar appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

