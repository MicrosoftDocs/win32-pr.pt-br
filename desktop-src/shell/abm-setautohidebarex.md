---
description: Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Essa mensagem estende ABM \_ SETAUTOHIDEBAR permitindo que você especifique um monitor específico, para uso em várias situações de monitor.
title: Mensagem de ABM_SETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104989462"
---
# <a name="abm_setautohidebarex-message"></a>\_Mensagem ABM SETAUTOHIDEBAREX

Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Essa mensagem estende [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) permitindo que você especifique um monitor específico, para uso em várias situações de monitor.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Defina o membro **lParam** como **true** para registrar AppBar ou **false** para cancelar o registro. Você deve especificar os membros **cbSize**, **HWND**, **uEdge**, **RC** e **lParam** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se um AutoOcultar AppBar já estiver registrado para a borda especificada no monitor especificado.

## <a name="remarks"></a>Comentários

O sistema permite apenas um AppBar de AutoOcultar para cada borda de cada monitor. O monitor é determinado pelo membro **RC** e a borda é determinada pelo membro **UEdge** da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> </dl>

 

 




