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
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="4a580-103">Recuperando dados de rastreamento de eventos adicionais</span><span class="sxs-lookup"><span data-stu-id="4a580-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="4a580-104">Depois de ter iniciado uma sessão de rastreamento de eventos, você pode usar o [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para instruir o sistema a retornar dados adicionais de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a580-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="4a580-105">As informações adicionais serão colocadas na seção de dados estendidos do rastreamento de eventos relevante.</span><span class="sxs-lookup"><span data-stu-id="4a580-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="4a580-106">O procedimento a seguir descreve como usar a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para recuperar dados adicionais de uma sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a580-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="4a580-107">**Para recuperar dados de rastreamento de eventos adicionais**</span><span class="sxs-lookup"><span data-stu-id="4a580-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="4a580-108">Inicie sua sessão com uma chamada para [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="4a580-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="4a580-109">Para obter mais informações, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="4a580-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="4a580-110">Chame [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para definir dados de rastreamento de eventos adicionais.</span><span class="sxs-lookup"><span data-stu-id="4a580-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="4a580-111">Use a [**enumeração \_ \_ classe de informações de evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) no parâmetro *ClassInformation* para descrever as informações adicionais que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="4a580-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="4a580-112">O exemplo a seguir descreve como chamar [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), usando o identificador de sessão retornado da chamada para [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e o valor de **TraceProviderBinaryTracking** da **\_ \_ classe de informações de evento**.</span><span class="sxs-lookup"><span data-stu-id="4a580-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="4a580-113">Como alternativa, você pode usar [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) para recuperar informações sobre as configurações de sessão de rastreamento de eventos atuais.</span><span class="sxs-lookup"><span data-stu-id="4a580-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="4a580-114">Como [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), o [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa a enumeração de [**\_ \_ classe de informações de evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) para descrever quais informações recuperar do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a580-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
