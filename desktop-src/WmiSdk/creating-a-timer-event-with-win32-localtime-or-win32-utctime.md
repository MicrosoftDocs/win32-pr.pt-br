---
description: Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as classes Win32 LocalTime ou \_ Win32 UTCTime para receber \_ uma notificação por tempo.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Criando um evento de temporizador com Win32_LocalTime ou Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f2dc2c3cbec2b87693920c0ed5ca113f7e6a04c9648f0ef2cc4bca9b4fa90f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612406"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Criando um evento de temporizador com Win32 \_ LocalTime ou Win32 \_ UTCTime

Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as classes [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) para receber uma notificação por tempo. O método intrínseco é uma maneira recomendada de gerar eventos com tempo, pois é consistente com o restante do modelo de evento da Microsoft e dá suporte a condições complexas de agendamento.

As [**classes Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) e [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) são classes singleton no \\ namespace raiz cimv2 que representam o relógio do sistema. Quando consultado, **Win32 \_ LocalTime** retorna a hora atual no momento da recuperação de dados em um relógio de 24 horas com referência local. A **classe Win32 \_ UTCTime** retorna a hora atual com referência UTC.

**Para gerar eventos com tempo ou repetição com Win32 \_ LocalTime ou Win32 \_ UTCTime**

-   Configurar um filtro de evento de notificação intrínseco [**para Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que solicita notificação para uma data e hora específicas.

Por exemplo, se a hora local em Horário de Verão for 16h e o local é GMT -8, [**Win32 \_ LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) retorna 16 e [**Win32 \_ UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) retorna 23.

O exemplo de código a seguir descreve como criar um filtro de evento que sinaliza um evento de repetição todos os dias à meia-noite.

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
