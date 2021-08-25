---
description: Notifica os aplicativos de que o computador está prestes a entrar em um estado suspenso.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: PBT_APMSUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb3634765e6c0f863beb0c7a1c16af29cadae18ef14796e9ef01a0c8edec36a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961666"
---
# <a name="pbt_apmsuspend-event"></a>Evento PBT \_ APMSUSPEND

Notifica os aplicativos de que o computador está prestes a entrar em um estado suspenso. Esse evento normalmente é transmitido quando todos os aplicativos e drivers instanciáveis **retornaram TRUE** para um evento [anterior do PBT \_ APMQUERYSUSPEND.](pbt-apmquerysuspend.md)

Uma janela recebe esse evento por meio da [**mensagem WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) Os *parâmetros wParam* *e lParam* são definidos conforme descrito a seguir.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
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

| Valor                                                                                                                                                                                                                         | Significado                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deve processar esse evento concluindo todas as tarefas necessárias para salvar dados.

O sistema permite aproximadamente dois segundos para um aplicativo lidar com essa notificação. Se um aplicativo ainda estiver executando operações depois que sua loteação de tempo tiver expirado, o sistema poderá interromper o aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Critérios de avaliação do sistema](system-sleep-criteria.md)
</dt> <dt>

[Eventos de a wake-up do sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de gerenciamento de energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**Setsystempowerstate**](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




