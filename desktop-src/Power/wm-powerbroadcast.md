---
description: Notifica os aplicativos que um evento de gerenciamento de energia ocorreu.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Mensagem de WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396501"
---
# <a name="wm_powerbroadcast-message"></a>Mensagem do WM \_ POWERBROADCAST

Notifica os aplicativos que um evento de gerenciamento de energia ocorreu.

Uma janela recebe essa mensagem por meio de sua função **WindowProc** .


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
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

| Valor                                                                                                                                                                                                                                          | Significado                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>* * * WM \_ POWERBROADCAST * *</dt> * * <dt>536 (0x218)</dt> </dl> | Identificador de mensagem.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

O evento de gerenciamento de energia. Esse parâmetro pode ser um dos seguintes identificadores de evento.



| Evento                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | O status de energia foi alterado.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | A operação está sendo retomada automaticamente de um estado de baixa energia. Essa mensagem é enviada toda vez que o sistema é retomado.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | A operação está sendo retomada de um estado de baixa energia. Essa mensagem será enviada após [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) se a retomada for disparada pela entrada do usuário, como pressionar uma tecla.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | O sistema está suspendendo a operação.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Um evento de alteração de configuração de energia foi recebido. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Os dados específicos do evento. Para a maioria dos eventos, esse parâmetro é reservado e não usado.

Se o parâmetro *wParam* for [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), o parâmetro *lParam* será um ponteiro para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deve retornar **true** se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

O sistema sempre envia uma mensagem [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) sempre que o sistema é retomado. Se o sistema for retomado em resposta à entrada do usuário, como pressionar uma tecla, o sistema também enviará uma mensagem **PBT \_ APMRESUMESUSPEND** depois de enviar PBT \_ APMRESUMEAUTOMATIC.

**WM \_** As mensagens POWERBROADCAST não fazem distinção entre Estados de baixa energia diferentes. Um aplicativo pode determinar apenas que o sistema está entrando ou foi retomado de um estado de baixa energia; Ele não pode determinar o estado de energia específico. O sistema registra os detalhes sobre as transições de estado de energia no log de eventos do sistema do Windows.

Para impedir que o sistema faça a transição para um estado de baixa energia no Windows Vista, um aplicativo deve chamar [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar ao sistema que ele está em uso.

As seguintes mensagens não têm suporte em nenhum dos sistemas operacionais especificados na seção requisitos:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_Mensagens POWERBROADCAST do WM](wm-powerbroadcast-messages.md)
</dt> <dt>

[Mensagens de gerenciamento de energia](power-management-messages.md)
</dt> </dl>

 

 




