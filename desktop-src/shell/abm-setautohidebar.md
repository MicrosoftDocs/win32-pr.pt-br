---
description: Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.
title: Mensagem de ABM_SETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967375"
---
# <a name="abm_setautohidebar-message"></a>\_Mensagem ABM SETAUTOHIDEBAR

Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.

> [!Note]  
> Para registrar ou cancelar o registro de um AutoOcultar AppBar em um monitor específico, use [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Defina o membro **lParam** como **true** para registrar o AppBar ou **false** para cancelar o registro. Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **lParam** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se um AutoOcultar AppBar já estiver registrado para a borda especificada.

## <a name="remarks"></a>Comentários

O sistema permite apenas um AppBar de AutoOcultar para cada borda da tela. Isso é determinado quando o membro **uEdge** da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) é definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




