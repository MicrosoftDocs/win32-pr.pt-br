---
description: Nota um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata. O aplicativo recebe esse comando por meio da mensagem SOLICITAÇÃO do WM \_ IME \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9376ff08e0406ff5505107ea1a04cf4e62898660065a8c7fdd54a1b8606850c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810109"
---
# <a name="imr_candidatewindow-notification-code"></a>Código de notificação \_ IMR CANDIDATEWINDOW

Nota um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata. O aplicativo recebe esse comando por meio da mensagem [**SOLICITAÇÃO do WM \_ IME \_**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para um buffer que contém uma [**estrutura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) Seu **membro dwIndex** contém o índice para a janela candidata referenciada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará um valor diferente de zero se o aplicativo preencher a [**estrutura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) Caso contrário, o comando retornará 0.

## <a name="remarks"></a>Comentários

Esse comando pode ser enviado pelo IME para uma janela que desobstruiu o sinalizador ISC \_ SHOWUICANDIDATEWINDOW no manipulador de [**mensagens \_ \_ SETCONTEXT do WM IME.**](wm-ime-setcontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de Métodos de Entrada](input-method-manager-commands.md)
</dt> <dt>

[**Candidateform**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**SOLICITAÇÃO \_ DO WM IME \_**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




