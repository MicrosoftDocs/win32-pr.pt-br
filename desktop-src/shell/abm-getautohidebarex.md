---
description: Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Essa mensagem estende ABM \_ GETAUTOHIDEBAR permitindo que você especifique um monitor específico, para uso em várias situações de monitor.
title: Mensagem de ABM_GETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225235"
---
# <a name="abm_getautohidebarex-message"></a>\_Mensagem ABM GETAUTOHIDEBAREX

Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Essa mensagem estende [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) permitindo que você especifique um monitor específico, para uso em várias situações de monitor.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica a borda e o monitor da tela. Você deve especificar os membros **cbSize**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para o AutoOcultar AppBar. O valor de retorno será **nulo** se ocorrer um erro ou se nenhuma AppBar de AutoOcultar estiver associada à borda fornecida do monitor especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




