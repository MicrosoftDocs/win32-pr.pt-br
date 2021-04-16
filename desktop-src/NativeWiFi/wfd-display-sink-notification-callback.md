---
description: Define a função de retorno de chamada&\# 8212; que você implementa em seu aplicativo&\# 8212; que foi especificado para a função WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK função de retorno de chamada (Wfdsink. h)
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
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751097"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Função de retorno de chamada de notificação do coletor de \_ vídeo WFD \_ \_ \_

A função de **retorno de chamada de \_ notificação do coletor de vídeo \_ \_ \_ WFD** define a função de retorno de chamada, que você implementa em seu aplicativo — que foi especificada para a função [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .

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

*pvContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro de contexto opcional passado para a função de retorno de chamada.

</dd> <dt>

*pNotification* \[ no\]
</dt> <dd>

Um ponteiro para uma struct que contém dados sobre a notificação do coletor de exibição.

</dd> <dt>

*pNotificationResult* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma struct que contém dados que seu aplicativo pode definir opcionalmente para indicar o resultado do processamento da notificação do coletor de exibição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




