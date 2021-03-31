---
title: Mensagem de WM_MENUCHAR (WinUser. h)
description: Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhum mnemônico ou tecla de aceleração. Essa mensagem é enviada para a janela que possui o menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menus de mensagens e outros recursos
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
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645232"
---
# <a name="wm_menuchar-message"></a>Mensagem do WM \_ MENUCHAR

Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhum mnemônico ou tecla de aceleração. Essa mensagem é enviada para a janela que possui o menu.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o código de caractere que corresponde à chave que o usuário pressionou.

A palavra de ordem superior especifica o tipo de menu ativo. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                 | Significado                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ 0x00000010L pop-up**</dt> <dt></dt> </dl>       | Um menu suspenso, submenu ou menu de atalho.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | O menu janela.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o menu ativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo que processa essa mensagem deve retornar um dos valores a seguir na palavra de ordem superior do valor de retorno.



| Código/valor de retorno                                                                                                                                  | Descrição                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ PERTO**</dt> de <dt>1</dt> </dl>   | Informa ao sistema que ele deve fechar o menu ativo.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXECUTAR**</dt> <dt>2</dt> </dl> | Informa ao sistema que ele deve escolher o item especificado na palavra de ordem inferior do valor de retorno. A janela do proprietário recebe uma mensagem de [**\_ comando do WM**](wm-command.md) .<br/> |
| <dl> <dt>**MNC \_ IGNORAR**</dt> <dt>0</dt> </dl>  | Informa ao sistema que ele deve descartar o caractere que o usuário pressionou e criar um bipe curto no alto-falante do sistema.<br/>                                                       |
| <dl> <dt>**MNC \_ Selecione**</dt> <dt>3</dt> </dl>  | Informa ao sistema que ele deve selecionar o item especificado na palavra de ordem inferior do valor de retorno. <br/>                                                                       |



 

## <a name="remarks"></a>Comentários

A palavra de ordem inferior será ignorada se a palavra de ordem superior contiver 0 ou 1.

Um aplicativo deve processar essa mensagem quando um acelerador é usado para selecionar um item de menu que exibe um bitmap.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

