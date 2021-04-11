---
description: Os dados de chamada são um buffer de tamanho de várias variantes que pode ser usado para acumular informações sobre uma sessão de comunicações. Essas informações ficam disponíveis para todos os aplicativos que possuem ou monitoram a sessão.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Dados de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296601"
---
# <a name="call-data"></a><span data-ttu-id="3678c-104">Dados de chamada</span><span class="sxs-lookup"><span data-stu-id="3678c-104">Call Data</span></span>

<span data-ttu-id="3678c-105">Os dados de chamada são um buffer de tamanho de várias variantes que pode ser usado para acumular informações sobre uma sessão de comunicações.</span><span class="sxs-lookup"><span data-stu-id="3678c-105">Call data is a variably sized buffer that can be used to accumulate information about a communications session.</span></span> <span data-ttu-id="3678c-106">Essas informações ficam disponíveis para todos os aplicativos que possuem ou monitoram a sessão.</span><span class="sxs-lookup"><span data-stu-id="3678c-106">This information becomes available to all applications that own or monitor the session.</span></span>

<span data-ttu-id="3678c-107">Por exemplo, o manipulador inicial de uma sessão de entrada pode solicitar e inserir informações de conta do cliente em um buffer de dados de chamada, e os manipuladores subsequentes não precisariam repetir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3678c-107">For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.</span></span>

<span data-ttu-id="3678c-108">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="3678c-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3678c-109">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** e **DwCallDataOffset** Members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* set to LINECALLINFOSTATE \_ CALLDATA).</span><span class="sxs-lookup"><span data-stu-id="3678c-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).</span></span>

<span data-ttu-id="3678c-110">**TAPI 3. x:** Consulte [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** membro do [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent:: get \_ A causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) retorna o membro **\_ CALLDATA do CIC** da [**\_ causa CALLINFOCHANGE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span><span class="sxs-lookup"><span data-stu-id="3678c-110">**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span></span>

 

 
