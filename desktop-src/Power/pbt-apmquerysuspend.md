---
description: Solicita permissão para suspender o computador. Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e8063ce68a88c8a39cb6f9ab8a4f559aed41242eaae25fab616ace8793b16ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143379"
---
# <a name="pbt_apmquerysuspend-event"></a>Evento PBT \_ APMQUERYSUSPEND

\[PBT APMQUERYSUSPEND está disponível para uso nos sistemas operacionais \_ especificados na seção Requisitos. O suporte para esse evento foi removido no Windows Vista. Em vez disso, use [**SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)\]

Solicita permissão para suspender o computador. Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.

Uma janela recebe esse evento por meio da [**mensagem WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) Os *parâmetros wParam* *e lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Um alça para janela.

</dd> <dt>*uMsg*</dt> <dd> 

| Valor                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador de mensagem.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valor                                                                                                                                                                                                                                        | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Os sinalizadores de ação. Se o bit 0 for 1, o aplicativo poderá solicitar instruções ao usuário sobre como se preparar para a suspensão; caso contrário, o aplicativo deverá se preparar sem interação do usuário. Todos os outros valores de bit são reservados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE** para conceder a solicitação de suspensão. Para negar a solicitação, retorne **BROADCAST \_ QUERY \_ DENY**.

## <a name="remarks"></a>Comentários

Um aplicativo deve processar esse evento o mais rápido possível. O aplicativo pode solicitar instruções ao usuário sobre como se preparar para suspensão somente se o bit 0 no *parâmetro Flags* estiver definido. No entanto, se essa mensagem for emitida porque o usuário está fechando a tampa do laptop, não será possível solicitar ao usuário. Os aplicativos devem respeitar que o usuário espere um determinado comportamento ao fechar a tampa do laptop ou pressionar o botão de energia e permitir que a transição seja bem-sucedida.

O sistema permite aproximadamente 20 segundos para um aplicativo remover a mensagem [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) que está enviando o evento PBT APMQUERYSUSPEND da fila de mensagens do \_ aplicativo. Se um aplicativo não remover a mensagem de sua fila em menos de 20 segundos, o sistema assumirá que o aplicativo está em um estado sem resposta e que o aplicativo concorda com a solicitação de espera. Aplicativos que não processam suas filas de mensagens podem ter suas operações interrompidas. Depois de remover a mensagem da fila de mensagens, um aplicativo pode levar o tempo necessário para executar as operações necessárias antes de entrar no estado de espera. Todas as operações que podem levar mais de 20 segundos devem ser executadas neste momento, pois o sistema permite que apenas 20 segundos para que as operações sejam concluídas durante o processamento do [PBT \_ APMSUSPEND.](pbt-apmsuspend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                                    |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de a wake-up do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




