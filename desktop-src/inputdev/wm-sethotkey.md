---
title: Mensagem de WM_SETHOTKEY (WinUser. h)
description: Enviado a uma janela para associar uma tecla de acesso à janela. Quando o usuário pressiona a tecla de acesso, o sistema ativa a janela.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Entrada de mouse e teclado de mensagem WM_SETHOTKEY
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6c9d4bdb4a59181fe3a413cca6861bc3663367cca9e7b34e0647de88978b0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482513"
---
# <a name="wm_sethotkey-message"></a>\_Mensagem de SETtecla do WM

Enviado a uma janela para associar uma tecla de acesso à janela. Quando o usuário pressiona a tecla de acesso, o sistema ativa a janela.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o código de chave virtual a ser associado à janela.

A palavra de ordem superior pode ser um ou mais dos seguintes valores de CommCtrl. h.

A definição de *wParam* como **NULL** remove a tecla de acesso associada a uma janela.



| Valor                                                                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>             | tecla ALT<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_ CONTROLE**</dt> <dt>0x02</dt> </dl> | Tecla CTRL<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> ext. </dl>             | Chave estendida<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ SHIFT**</dt> <dt>0x01</dt> </dl>       | Tecla SHIFT<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um dos seguintes.



| Valor retornado                                                                  | Descrição                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | A função não é bem-sucedida; a tecla de acesso é inválida.<br/>                        |
| <dl> <dt>0</dt> </dl>  | A função não é bem-sucedida; a janela é inválida.<br/>                         |
| <dl> <dt>1</dt> </dl>  | A função é bem-sucedida e nenhuma outra janela tem a mesma tecla de atalho.<br/>        |
| <dl> <dt>2</dt> </dl>  | A função foi bem-sucedida, mas outra janela já tem a mesma tecla de atalho.<br/> |



 

## <a name="remarks"></a>Comentários

Uma tecla de acesso não pode ser associada a uma janela filho.

**VK \_ ESCAPE**, **\_ espaço VK** e **\_ guia VK** são teclas de acesso inválidas.

Quando o usuário pressiona a tecla de atalho, o sistema gera uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) com *wParam* igual a **sc \_ teclaize** e *lParam* igual ao identificador da janela. Se essa mensagem for passada para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o sistema trará o último Popup ativo da janela (se existir) ou a própria janela (se não houver nenhuma janela pop-up) para o primeiro plano.

Uma janela pode ter apenas uma tecla de acesso. Se a janela já tiver uma tecla de acesso associada a ela, a nova tecla de acesso substituirá a antiga. Se mais de uma janela tiver a mesma tecla de atalho, a janela ativada pela tecla de acesso será aleatória.

Essas teclas de acesso não estão relacionadas às teclas de acesso definidas por [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_**](wm-gethotkey.md)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

