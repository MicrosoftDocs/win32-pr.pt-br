---
description: Notifica os aplicativos que o BIOS do APM sinalizou um evento de OEM do APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Evento de PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92feb840e69c3a7e560d7bc71a0a5e4746ae5677920010f0251a1b951ddb8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961646"
---
# <a name="pbt_apmoemevent-event"></a>\_Evento PBT APMOEMEVENT

\[PBT \_ APMOEMEVENT está disponível para uso nos sistemas operacionais especificados na seção requisitos. o suporte para esse evento foi removido no Windows Vista.\]

Notifica os aplicativos que o BIOS do APM sinalizou um evento de OEM do APM.

Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
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

| Valor                                                                                                                                                                                                                             | Significado                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O código de evento definido pelo OEM que foi sinalizado pelo BIOS do APM do sistema. Os códigos de evento OEM estão no intervalo 0200h-02FFh.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Como nem todas as implementações do BIOS do APM fornecem notificações de eventos do OEM, esse evento pode nunca ser transmitido em alguns computadores.

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

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[**POWERBROADCAST do WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




