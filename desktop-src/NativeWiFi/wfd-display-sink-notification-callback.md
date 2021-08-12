---
description: Define a função de retorno de chamada&8212;que você implementa em seu aplicativo \#&8212;que foi especificada para a \# função WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK função de retorno de chamada (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: 7066f45b714c28b53747d0d0f1851bd94ac2ac902e5b4adba1d0746e8328b3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619971"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Função de retorno de chamada de retorno de chamada WFD \_ DISPLAY \_ SINK \_ \_ NOTIFICATION

A **função WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK** define a função de retorno de chamada , que você implementa em seu aplicativo, que foi especificada para a [**função WFDStartDisplaySink.**](wfdstartdisplaysink.md)

## <a name="syntax"></a>Sintaxe


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvContext* \[ in, opcional\]
</dt> <dd>

Um ponteiro de contexto opcional passado para a função de retorno de chamada.

</dd> <dt>

*pNotification* \[ Em\]
</dt> <dd>

Um ponteiro para um struct que contém dados sobre a notificação do sink de exibição.

</dd> <dt>

*pNotificationResult* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para um struct que contém dados que seu aplicativo pode definir opcionalmente para indicar o resultado do processamento da notificação do sink de exibição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




