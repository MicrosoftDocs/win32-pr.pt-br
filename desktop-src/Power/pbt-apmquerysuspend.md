---
description: Solicita permissão para suspender o computador. Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento de PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828366"
---
# <a name="pbt_apmquerysuspend-event"></a>\_Evento PBT APMQUERYSUSPEND

\[PBT \_ APMQUERYSUSPEND está disponível para uso nos sistemas operacionais especificados na seção requisitos. O suporte para esse evento foi removido no Windows Vista. Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) em vez disso.\]

Solicita permissão para suspender o computador. Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.


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

*HWND* 
</dt> <dd>

Um identificador para a janela.

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

Os sinalizadores de ação. Se o bit 0 for 1, o aplicativo poderá solicitar instruções ao usuário sobre como se preparar para a suspensão; caso contrário, o aplicativo deve se preparar sem interação com o usuário. Todos os outros valores de bit são reservados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true** para conceder a solicitação para suspender. Para negar a solicitação, retorne a **consulta de difusão \_ \_ negar**.

## <a name="remarks"></a>Comentários

Um aplicativo deve processar esse evento o mais rápido possível. O aplicativo pode solicitar instruções ao usuário sobre como se preparar para a suspensão somente se o bit 0 no parâmetro *flags* estiver definido. No entanto, se essa mensagem for emitida porque o usuário está fechando a tampa do laptop, não será possível solicitar o usuário. Os aplicativos devem respeitar que o usuário espera um determinado comportamento quando fecham a tampa do laptop ou pressionam o botão de energia e permitem que a transição tenha sucesso.

O sistema permite que aproximadamente 20 segundos para um aplicativo remova a mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) que está enviando o \_ evento PBT APMQUERYSUSPEND da fila de mensagens do aplicativo. Se um aplicativo não remover a mensagem de sua fila em menos de 20 segundos, o sistema irá pressupor que o aplicativo está em um estado não responsivo e que o aplicativo concorda com a solicitação de suspensão. Os aplicativos que não processam suas filas de mensagens podem ter suas operações interrompidas. Depois de remover a mensagem da fila de mensagens, um aplicativo pode levar tanto tempo quanto necessário para executar as operações necessárias antes de entrar no estado de suspensão. Qualquer operação que possa demorar mais do que 20 segundos deve ser executada no momento, uma vez que o sistema permite que apenas 20 segundos para que as operações sejam concluídas durante o processamento do [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                                           |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de ativação do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




