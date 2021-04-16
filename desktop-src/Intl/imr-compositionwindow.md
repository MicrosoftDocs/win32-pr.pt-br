---
description: Notifica um aplicativo quando um IME selecionado precisa de informações sobre a janela de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros definidos, conforme mostrado abaixo.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752271"
---
# <a name="imr_compositionwindow-notification-code"></a>Código de notificação do IMR \_ COMPOSITIONWINDOW

Notifica um aplicativo quando um IME selecionado precisa de informações sobre a janela de composição. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros definidos, conforme mostrado abaixo.


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ COMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para um buffer que contém uma estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) . Caso contrário, o comando retornará 0.

## <a name="remarks"></a>Comentários

Esse comando pode ser enviado pelo IME para uma janela que limpou o \_ sinalizador SHOWUICOMPOSITIONWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> <dt>

[**SetContext IME do WM \_ \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




