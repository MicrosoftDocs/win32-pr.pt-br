---
title: Mensagem de WM_MENUGETOBJECT (WinUser. h)
description: Enviado ao proprietário de um menu de arrastar e soltar quando o cursor do mouse entra em um item de menu ou se move do centro do item para a parte superior ou inferior do item.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499837"
---
# <a name="wm_menugetobject-message"></a>Mensagem do WM \_ MENUGETOBJECT

Enviado ao proprietário de um menu de arrastar e soltar quando o cursor do mouse entra em um item de menu ou se move do centro do item para a parte superior ou inferior do item.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo deve retornar um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                | Descrição                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_ NOERROR**</dt> <dt>0x00000001</dt> </dl>     | Um ponteiro de interface foi retornado no membro **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)<br/> |
| <dl> <dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt> </dl> | Não há suporte para a interface.<br/>                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral dos menus](menus.md)
</dt> </dl>

 

 





