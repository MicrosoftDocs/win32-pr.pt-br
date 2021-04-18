---
description: A \_ mensagem de EndSession do WM é enviada para um aplicativo depois que o sistema processa os resultados da mensagem do WM \_ QUERYENDSESSION. A \_ mensagem de EndSession do WM informa ao aplicativo se a sessão está terminando.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Mensagem de WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755544"
---
# <a name="wm_endsession-message"></a>\_Mensagem de ENDsession do WM

A mensagem de **\_ EndSession do WM** é enviada para um aplicativo depois que o sistema processa os resultados da mensagem do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) . A mensagem de **\_ EndSession do WM** informa ao aplicativo se a sessão está terminando.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
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

O identificador de **\_ EndSession do WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Se a sessão estiver sendo finalizada, esse parâmetro será **true**; a sessão pode terminar a qualquer momento depois que todos os aplicativos forem retornados do processamento dessa mensagem. Caso contrário, será **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro pode ser um ou mais dos valores a seguir. Se esse parâmetro for 0, o sistema está sendo desligado ou reiniciado (não é possível determinar qual evento está ocorrendo).



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDsession \_ CLOSEAPP**</dt> <dt>0x1</dt> </dl>        | Se *wParam* for **true**, o aplicativo deverá ser desligado. Todos os dados devem ser salvos automaticamente sem avisar o usuário (para obter mais informações, consulte comentários). O Gerenciador de reinicialização envia essa mensagem quando o aplicativo está usando um arquivo que precisa ser substituído, quando ele deve atender ao sistema ou quando os recursos do sistema são esgotados. O aplicativo será reiniciado se tiver sido registrado para reinicialização usando a função [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . Para obter mais informações, consulte [diretrizes para aplicativos](../rstmgr/guidelines-for-applications.md). <br/> Se *wParam* for **false**, o aplicativo não deverá ser desligado.<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDsession \_**</dt> <dt>0x40000000</dt> crítico </dl> | O aplicativo é forçado a desligar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDsession \_ LOGOFF**</dt> <dt>0x80000000</dt> </dl>       | O usuário está fazendo logoff. Para obter mais informações, consulte [fazendo logoff](logging-off.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Observe que esse parâmetro é uma máscara de bits. Para testar esse valor, use uma operação bit-wise; Não teste a igualdade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Os aplicativos que têm dados não salvos podem salvar os dados em um local temporário e restaurá-los na próxima vez que o aplicativo for iniciado. É recomendável que os aplicativos salvem seus dados e Estados com frequência; por exemplo, salve automaticamente os dados entre as operações de salvamento iniciadas pelo usuário para reduzir a quantidade de dados a serem salvos no desligamento.

O aplicativo não precisa chamar a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ou [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) quando a sessão está terminando.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**QUERYENDSESSION do WM \_**](wm-queryendsession.md)
</dt> </dl>

 

 
