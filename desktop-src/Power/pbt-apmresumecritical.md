---
description: Notifica os aplicativos de que o sistema retomou a operação.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento de PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13214a97e99954d0649df0647bdf6ee3823b91926c0f2f2dc1212fa780a7b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961697"
---
# <a name="pbt_apmresumecritical-event"></a>\_Evento PBT APMRESUMECRITICAL

\[PBT \_ APMRESUMECRITICAL está disponível para uso nos sistemas operacionais especificados na seção requisitos. o suporte para esse evento foi removido no Windows Vista. Em vez disso, use [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .\]

Notifica os aplicativos de que o sistema retomou a operação. Esse evento pode indicar que alguns ou todos os aplicativos não receberam um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) . Por exemplo, esse evento pode ser transmitido após uma suspensão crítica causada por uma bateria com falha.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
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

| Valor                                                                                                                                                                                                                                              | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Como uma suspensão crítica ocorre sem notificação anterior, os recursos e os dados disponíveis anteriormente poderão não estar presentes quando o aplicativo receber esse evento. O aplicativo deve tentar restaurar seu estado da melhor forma que puder. Durante uma suspensão crítica, o sistema mantém o estado dos discos rígidos locais e DRAM, mas pode não manter conexões de rede. Um aplicativo pode precisar executar uma ação em relação aos arquivos que estavam abertos na rede antes da suspensão crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de ativação do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




