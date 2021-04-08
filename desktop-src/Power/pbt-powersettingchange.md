---
description: Evento de alteração de configuração de energia enviado com uma mensagem de janela do WM \_ POWERBROADCAST ou em um retorno de chamada de notificação HandlerEx para serviços.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Evento de PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828364"
---
# <a name="pbt_powersettingchange-event"></a>\_Evento PBT POWERSETTINGCHANGE

Evento de alteração de configuração de energia enviado com uma mensagem de janela do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) ou em um retorno de chamada de notificação [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) para serviços.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
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

| Valor                                                                                                                                                                                                                                                        | Significado                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> <dt>

[**configuração de POWERBROADCAST \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

