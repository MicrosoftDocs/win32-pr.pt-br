---
description: Notifica os aplicativos de que o sistema retomou a operação depois de ser suspenso.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento de PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756693"
---
# <a name="pbt_apmresumesuspend-event"></a>\_Evento PBT APMRESUMESUSPEND

Notifica os aplicativos de que o sistema retomou a operação depois de ser suspenso.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
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

| Valor                                                                                                                                                                                                                                           | Significado                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo poderá receber esse evento somente se ele recebeu o evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de o computador ser suspenso. Caso contrário, o aplicativo receberá um evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .

Se o sistema for ativado devido à atividade do usuário (como pressionar o botão de energia) ou se o sistema detectar a interação do usuário no console físico (como entrada do mouse ou do teclado) após a ativação autônoma, o sistema primeiro transmite o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) e, em seguida, transmite o \_ evento PBT APMRESUMESUSPEND. Além disso, o sistema ativa a exibição. Seu aplicativo deve reabrir os arquivos que ele fechou quando o sistema entrou em suspensão e se preparar para a entrada do usuário.

Se o sistema for ativado devido a um sinal de ativação externo (ativação remota), o sistema transmitirá apenas o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) . O \_ evento PBT APMRESUMESUSPEND não é enviado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de ativação do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




