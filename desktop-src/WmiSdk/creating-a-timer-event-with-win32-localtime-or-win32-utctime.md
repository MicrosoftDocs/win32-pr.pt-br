---
description: Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as \_ classes Win32 localtime ou Win32 \_ UTCTime para receber uma notificação cronometrada.
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
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171451"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Criando um evento de temporizador com Win32 \_ localtime ou Win32 \_ UTCTime

Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) para receber uma notificação cronometrada. O método intrínseco é uma maneira recomendada de gerar eventos cronometrados, pois é consistente com o restante do modelo de evento da Microsoft e dá suporte a condições de agendamento complexas.

As classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) e [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) são classes singleton no namespace raiz \\ cimv2 que representam o relógio do sistema. Quando consultado, o **Win32 \_ localtime** retorna a hora atual no momento da recuperação de dados em um relógio de 24 horas com referência local. A classe **Win32 \_ UTCTime** retorna a hora atual com referência UTC.

**Para gerar eventos cronometrados ou repetidos com Win32 \_ localtime ou Win32 \_ UTCTime**

-   Configure um filtro de eventos de notificação intrínseco para [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que solicita a notificação para uma data e hora específicas.

Por exemplo, se a hora local em horário de verão é de 4 horas e o local é GMT-8, o [**Win32 \_ localtime. hora**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) retorna 16 e o [**Win32 \_ UTCTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) retorna 23.

O exemplo de código a seguir descreve como criar um filtro de eventos que sinaliza um evento repetido todos os dias à meia-noite.

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

 

 
