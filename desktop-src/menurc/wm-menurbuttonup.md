---
title: Mensagem de WM_MENURBUTTONUP (WinUser. h)
description: Enviado quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295918"
---
# <a name="wm_menurbuttonup-message"></a>Mensagem do WM \_ MENURBUTTONUP

Enviado quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item de menu no qual o botão direito do mouse foi liberado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o menu que contém o item.

</dd> </dl>

## <a name="remarks"></a>Comentários

A mensagem do **WM \_ MENURBUTTONUP** permite que os aplicativos forneçam um menu contextual também conhecido como menu de atalho para o item de menu especificado nesta mensagem. Para exibir um menu sensível ao contexto para um item de menu, chame a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) com o **TPM \_ recurse**.

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

 

 





