---
title: WM_MENUCHAR mensagem (Winuser.h)
description: Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhuma tecla mnemônica ou de acelerador. Essa mensagem é enviada para a janela que possui o menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d276418636857fb7ce76159111b8e8b24519235823225fccb68fa1523b4137d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869605"
---
# <a name="wm_menuchar-message"></a>Mensagem \_ WM MENUCHAR

Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhuma tecla mnemônica ou de acelerador. Essa mensagem é enviada para a janela que possui o menu.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem baixa especifica o código de caractere que corresponde à chave pressionada pelo usuário.

A palavra de ordem alta especifica o tipo de menu ativo. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                 | Significado                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>       | Um menu suspenso, submenu ou menu de atalho.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | O menu da janela.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o menu ativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo que processa essa mensagem deve retornar um dos valores a seguir na palavra de ordem alta do valor de retorno.



| Valor/código de retorno                                                                                                                                  | Descrição                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ CLOSE**</dt> <dt>1</dt> </dl>   | Informa ao sistema que ele deve fechar o menu ativo.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXECUTE**</dt> <dt>2</dt> </dl> | Informa ao sistema que ele deve escolher o item especificado na palavra de ordem baixa do valor de retorno. A janela proprietário recebe uma mensagem [**WM \_ COMMAND.**](wm-command.md)<br/> |
| <dl> <dt>**MNC \_ IGNORAR**</dt> <dt>0</dt> </dl>  | Informa ao sistema que ele deve descartar o caractere pressionado pelo usuário e criar um aviso curto no alto-falante do sistema.<br/>                                                       |
| <dl> <dt>**MNC \_ SELECT**</dt> <dt>3</dt> </dl>  | Informa ao sistema que ele deve selecionar o item especificado na palavra de ordem baixa do valor de retorno. <br/>                                                                       |



 

## <a name="remarks"></a>Comentários

A palavra de ordem baixa será ignorada se a palavra de ordem alta contiver 0 ou 1.

Um aplicativo deve processar essa mensagem quando um acelerador é usado para selecionar um item de menu que exibe um bitmap.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

