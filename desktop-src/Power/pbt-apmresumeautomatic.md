---
description: Notifica os aplicativos que o sistema está retomando do modo de suspensão ou hibernação. Esse evento é entregue toda vez que o sistema é retomado e não indica se um usuário está presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento de PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e66fcd2201e9fb3c4feeb135843e92a350303b89a5c5045836428b9a326a30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143339"
---
# <a name="pbt_apmresumeautomatic-event"></a>\_Evento PBT APMRESUMEAUTOMATIC

Notifica os aplicativos que o sistema está retomando do modo de suspensão ou hibernação. Esse evento é entregue toda vez que o sistema é retomado e não indica se um usuário está presente.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.

> [!Note]  
> em Windows 10, versão 1507 sistemas ou posteriores, se o sistema estiver retomando do modo de suspensão somente para entrar imediatamente em hibernação, esse evento não será entregue. Uma mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) não é enviada nesse caso.

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
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

| Valor                                                                                                                                                                                                                                                   | Significado                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se o sistema detectar qualquer atividade do usuário após a difusão PBT \_ APMRESUMEAUTOMATIC, ele transmitirá um evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) para permitir que os aplicativos saibam que podem retomar a interação total com o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de ativação do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




