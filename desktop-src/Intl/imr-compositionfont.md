---
description: Notifica um aplicativo quando um IME selecionado precisa de informações sobre a fonte usada pela janela de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros, conforme mostrado abaixo.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758791"
---
# <a name="imr_compositionfont-notification-code"></a>Código de notificação do IMR \_ COMPOSITIONFONT

Notifica um aplicativo quando um IME selecionado precisa de informações sobre a fonte usada pela janela de composição. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros, conforme mostrado abaixo.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ COMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para um buffer que contém uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . O aplicativo preenche os valores para a janela de composição atual.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Caso contrário, o comando retornará 0.

## <a name="remarks"></a>Comentários

Esse comando pode ser enviado pelo IME para uma janela que desmarcou o \_ sinalizador SHOWUICOMPOSITIONWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .

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

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> <dt>

[**SetContext IME do WM \_ \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 
