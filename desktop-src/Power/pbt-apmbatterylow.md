---
description: Notifica os aplicativos que a energia da bateria está baixa.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Evento de PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759352"
---
# <a name="pbt_apmbatterylow-event"></a>\_Evento PBT APMBATTERYLOW

\[PBT \_ APMBATTERYLOW está disponível para uso nos sistemas operacionais especificados na seção requisitos. O suporte para esse evento foi removido no Windows Vista. Em vez disso, use [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) .\]

Notifica os aplicativos que a energia da bateria está baixa.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
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

| Valor                                                                                                                                                                                                                                  | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado, deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse evento é transmitido quando o BIOS do APM do sistema sinaliza uma notificação de baixa bateria do APM. Como algumas implementações do BIOS do APM não fornecem notificações quando as baterias estão baixas, esse evento pode nunca ser transmitido em alguns computadores.

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

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




