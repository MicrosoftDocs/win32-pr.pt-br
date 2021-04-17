---
title: Mensagem de WM_MENUDRAG (WinUser. h)
description: Enviado ao proprietário de um menu de arrastar e soltar quando o usuário arrasta um item de menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761670"
---
# <a name="wm_menudrag-message"></a>Mensagem do WM \_ MENUDRAG

Enviado ao proprietário de um menu de arrastar e soltar quando o usuário arrasta um item de menu.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A posição do item no qual a operação de arrastar começou.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o menu que contém o item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo deve retornar um dos valores a seguir.



| Código/valor de retorno                                                                                                                                   | Descrição                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUAR**</dt> <dt>0</dt> </dl> | O menu deve permanecer ativo. Se o mouse for liberado, ele deverá ser ignorado.<br/> |
| <dl> <dt>**MND \_ Endmenu**</dt> <dt>1</dt> </dl>  | O menu deve ser encerrado.<br/>                                                      |



 

## <a name="remarks"></a>Comentários

O aplicativo pode chamar a função [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) em resposta a esta mensagem.

Para criar um menu do tipo "arrastar e soltar", chame [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) com **MNS \_ DRAGDROP**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

