---
description: A mensagem WM QUERYENDSESSION é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento \_ do sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: WM_QUERYENDSESSION mensagem (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6807a861ffb0670013a1d1f5b98a2f202e5d7470a6c306b3ed29c42baad6e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664206"
---
# <a name="wm_queryendsession-message"></a>Mensagem WM \_ QUERYENDSESSION

A **mensagem WM \_ QUERYENDSESSION** é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento do sistema. Se qualquer aplicativo retornar zero, a sessão não será encerrada. O sistema para de **enviar mensagens WM \_ QUERYENDSESSION** assim que um aplicativo retorna zero.

Depois de processar essa mensagem, o sistema envia a mensagem [**WM \_ ENDSESSION**](wm-endsession.md) com o parâmetro *wParam* definido para os resultados da mensagem **WM \_ QUERYENDSESSION.**

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Um alça para a janela.

</dd> <dt>

*Umsg* 
</dt> <dd>

O **\_ identificador WM QUERYENDSESSION.**

</dd> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro pode ser um ou mais dos valores a seguir. Se esse parâmetro for 0, o sistema será desligado ou reiniciado (não é possível determinar qual evento está ocorrendo).



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x00000001</dt> </dl> | O aplicativo está usando um arquivo que deve ser substituído, o sistema está sendo atendido ou os recursos do sistema estão esgotados. Para obter mais informações, consulte [Diretrizes para aplicativos](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_ PONTOS CRÍTICOS**</dt> <dt>0X40000000</dt> </dl> | O aplicativo é forçado a ser desligado.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LOGOFF**</dt> <dt>0x80000000</dt> </dl>       | O usuário está fazendo logo off. Para obter mais informações, consulte [Log Off](logging-off.md).<br/>                                                                                                                                   |



 

Observe que esse parâmetro é uma máscara de bits. Para testar esse valor, use uma operação bit a bit; não testar a igualdade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os aplicativos devem respeitar as intenções do usuário e retornar **TRUE.** Por padrão, a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna **TRUE** para esta mensagem.

Se o desligamento corromper o sistema ou a mídia que está sendo gravado, o aplicativo poderá retornar **FALSE.** No entanto, é uma boa prática respeitar as ações do usuário.

## <a name="remarks"></a>Comentários

Quando um aplicativo retorna **TRUE** para essa mensagem, ele recebe a mensagem [**WM \_ ENDSESSION,**](wm-endsession.md) independentemente de como os outros aplicativos respondem à mensagem **WM \_ QUERYENDSESSION.** Cada aplicativo deve retornar **TRUE** ou **FALSE** imediatamente após receber essa mensagem e adiar todas as operações de limpeza até receber a mensagem **WM \_ ENDSESSION.**

Os aplicativos podem exibir uma interface do usuário solicitando ao usuário informações no desligamento, no entanto, não é recomendável. Após cinco segundos, o sistema exibe informações sobre os aplicativos que estão impedindo o desligamento e permite que o usuário os encente. Por exemplo, Windows XP exibe uma caixa de diálogo, enquanto Windows Vista exibe uma tela inteira com informações adicionais sobre os aplicativos que bloqueiam o desligamento. Se o aplicativo tiver que bloquear ou adiar o desligamento do sistema, use a [**função ShutdownBlockReasonCreate.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) Para obter mais informações, consulte [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Os aplicativos de console podem usar [**a função SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para receber notificação de desligamento.

Os aplicativos de serviço podem usar [**a função RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para receber notificações de desligamento em uma rotina de manipulador.

## <a name="examples"></a>Exemplos

Para ver um exemplo, consulte [Log Off](logging-off.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho XP\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2003 \|\]<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fazendo logo off](logging-off.md)
</dt> <dt>

[Desligar](shutting-down.md)
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
