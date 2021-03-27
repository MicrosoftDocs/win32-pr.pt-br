---
description: Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.
title: Mensagem de ABM_GETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090036"
---
# <a name="abm_getautohidebar-message"></a>\_Mensagem ABM GETAUTOHIDEBAR

Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.

> [!Note]  
> Para consultar uma AutoOcultar AppBar em um monitor específico, use [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica a borda da tela. Você deve especificar os membros **cbSize** e **uEdge** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o AutoOcultar AppBar. O valor de retorno será **nulo** se ocorrer um erro ou se nenhuma AppBar de AutoOcultar estiver associada à borda especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




