---
description: Notifica os aplicativos que o sistema, normalmente, um computador pessoal alimentado por bateria, está prestes a entrar em um modo suspenso.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Mensagem de WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd525b4bf229fdb04dac4c1d1492a52dad44317344f58a2f0807ba9afbdc962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143179"
---
# <a name="wm_power-message"></a>Mensagem de energia do WM \_

Notifica os aplicativos que o sistema, normalmente, um computador pessoal alimentado por bateria, está prestes a entrar em um modo suspenso.

> [!Note]  
> A mensagem de **\_ energia do WM** está obsoleta. ele é fornecido apenas para compatibilidade com aplicativos baseados em Windows de 16 bits. Os aplicativos devem usar a mensagem [**\_ POWERBROADCAST do WM**](wm-powerbroadcast.md) .

 

Uma janela recebe essa mensagem por meio de sua função **WindowProc** .


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

O identificador de mensagem de **\_ energia do WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

A notificação de evento de energia. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**\_CRITICALRESUME PWR**</dt> </dl> | Indica que o sistema está retomando a operação depois de entrar no modo suspenso sem primeiro transmitir uma mensagem de notificação de **\_ SUSPENDREQUEST PWR** para o aplicativo. Um aplicativo deve executar as ações de recuperação necessárias.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**\_SUSPENDREQUEST PWR**</dt> </dl> | Indica que o sistema está prestes a entrar no modo suspenso.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**\_SUSPENDRESUME PWR**</dt> </dl>    | Indica que o sistema está retomando a operação depois de ter inserido o modo suspenso normalmente, ou seja, o sistema transmite uma mensagem de notificação de **\_ SUSPENDREQUEST PWR** para o aplicativo antes de o sistema ser suspenso. Um aplicativo deve executar as ações de recuperação necessárias.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor que um aplicativo retorna depende do valor do parâmetro *wParam* . Se *wParam* for **PWR \_ SUSPENDREQUEST**, o valor de retorno será **PWR \_ falha** ao impedir que o sistema entre no estado suspenso; caso contrário, será **PWR \_ OK**. Se *wParam* for **PWR \_ SUSPENDRESUME** ou **PWR \_ CRITICALRESUME**, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Essa mensagem é difundida somente para um aplicativo que está sendo executado em um sistema que está em conformidade com a especificação do BIOS (sistema de entrada/saída) básico do APM (gerenciamento avançado de energia). A mensagem é transmitida pelo driver de gerenciamento de energia para cada janela retornada pela função **EnumWindows** .

O modo suspenso é o estado em que ocorre a maior quantidade de economia de energia, mas todos os dados operacionais e parâmetros são preservados. O conteúdo de RAM (memória de acesso aleatório) é preservado, mas muitos dispositivos provavelmente serão desativados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




