---
description: A mensagem do WM \_ QUERYENDSESSION é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento do sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Mensagem de WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753707"
---
# <a name="wm_queryendsession-message"></a>Mensagem do WM \_ QUERYENDSESSION

A mensagem do **WM \_ QUERYENDSESSION** é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento do sistema. Se qualquer aplicativo retornar zero, a sessão não será encerrada. O sistema para de enviar mensagens do **WM \_ QUERYENDSESSION** assim que um aplicativo retorna zero.

Depois de processar essa mensagem, o sistema envia a mensagem de [**\_ EndSession do WM**](wm-endsession.md) com o parâmetro *wParam* definido para os resultados da mensagem **\_ QUERYENDSESSION do WM** .

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

O **identificador \_ QUERYENDSESSION do WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro pode ser um ou mais dos valores a seguir. Se esse parâmetro for 0, o sistema está sendo desligado ou reiniciado (não é possível determinar qual evento está ocorrendo).



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDsession \_ CLOSEAPP**</dt> <dt>0x00000001</dt> </dl> | O aplicativo está usando um arquivo que deve ser substituído, o sistema está sendo atendido ou os recursos do sistema estão esgotados. Para obter mais informações, consulte [diretrizes para aplicativos](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDsession \_**</dt> <dt>0x40000000</dt> crítico </dl> | O aplicativo é forçado a desligar.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDsession \_ LOGOFF**</dt> <dt>0x80000000</dt> </dl>       | O usuário está fazendo logoff. Para obter mais informações, consulte [fazendo logoff](logging-off.md).<br/>                                                                                                                                   |



 

Observe que esse parâmetro é uma máscara de bits. Para testar esse valor, use uma operação bit-wise; Não teste a igualdade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os aplicativos devem respeitar as intenções do usuário e retornar **true**. Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna **true** para esta mensagem.

Se o desligamento corromper o sistema ou a mídia que está sendo gravada, o aplicativo poderá retornar **false**. No entanto, é uma boa prática respeitar as ações do usuário.

## <a name="remarks"></a>Comentários

Quando um aplicativo retorna **true** para essa mensagem, ele recebe a mensagem de [**\_ EndSession do WM**](wm-endsession.md) , independentemente de como os outros aplicativos respondem à mensagem do **WM \_ QUERYENDSESSION** . Cada aplicativo deve retornar **true** ou **false** imediatamente após o recebimento dessa mensagem e adiar todas as operações de limpeza até receber a mensagem de **\_ EndSession do WM** .

Os aplicativos podem exibir uma interface do usuário solicitando as informações do usuário no desligamento, no entanto, isso não é recomendado. Após cinco segundos, o sistema exibe informações sobre os aplicativos que estão impedindo o desligamento e permite que o usuário os encerre. Por exemplo, o Windows XP exibe uma caixa de diálogo, enquanto o Windows Vista exibe uma tela inteira com informações adicionais sobre os aplicativos que bloqueiam o desligamento. Se seu aplicativo precisar bloquear ou adiar o desligamento do sistema, use a função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . Para obter mais informações, consulte [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Os aplicativos de console podem usar a função [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para receber a notificação de desligamento.

Os aplicativos de serviço podem usar a função [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para receber notificações de desligamento em uma rotina de manipulador.

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [fazendo logoff](logging-off.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fazendo logoff](logging-off.md)
</dt> <dt>

[Desligando](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**EndSession do WM \_**](wm-endsession.md)
</dt> </dl>

 

 
