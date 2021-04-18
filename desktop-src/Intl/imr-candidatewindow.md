---
description: Notfies um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758973"
---
# <a name="imr_candidatewindow-notification-code"></a>Código de notificação do IMR \_ CANDIDATEWINDOW

Notfies um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para um buffer que contém uma estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Seu membro **dwIndex** contém o índice para a janela candidata referenciada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Caso contrário, o comando retornará 0.

## <a name="remarks"></a>Comentários

Esse comando pode ser enviado pelo IME para uma janela que limpou o \_ sinalizador SHOWUICANDIDATEWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> <dt>

[**SetContext IME do WM \_ \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




