---
description: Depois de ter iniciado uma sessão de rastreamento de eventos, você pode usar o TraceSetInformation para instruir o sistema a retornar dados adicionais de rastreamento de eventos.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Recuperando dados de rastreamento de eventos adicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921102"
---
# <a name="retrieving-additional-event-tracing-data"></a>Recuperando dados de rastreamento de eventos adicionais

Depois de ter iniciado uma sessão de rastreamento de eventos, você pode usar o [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para instruir o sistema a retornar dados adicionais de rastreamento de eventos. As informações adicionais serão colocadas na seção de dados estendidos do rastreamento de eventos relevante.

O procedimento a seguir descreve como usar a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para recuperar dados adicionais de uma sessão de rastreamento de eventos.

**Para recuperar dados de rastreamento de eventos adicionais**

1.  Inicie sua sessão com uma chamada para [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Para obter mais informações, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

2.  Chame [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para definir dados de rastreamento de eventos adicionais.

    Use a [**enumeração \_ \_ classe de informações de evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) no parâmetro *ClassInformation* para descrever as informações adicionais que você deseja recuperar. O exemplo a seguir descreve como chamar [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), usando o identificador de sessão retornado da chamada para [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e o valor de **TraceProviderBinaryTracking** da **\_ \_ classe de informações de evento**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Como alternativa, você pode usar [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) para recuperar informações sobre as configurações de sessão de rastreamento de eventos atuais.

    Como [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), o [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa a enumeração de [**\_ \_ classe de informações de evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) para descrever quais informações recuperar do sistema.

 

 
