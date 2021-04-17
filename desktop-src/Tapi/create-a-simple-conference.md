---
description: O exemplo de código a seguir demonstra a criação de uma chamada de conferência simples. Para obter informações sobre videoconferência de multimídia de IP, consulte sobre a reunião de conferência de telefonia IP.
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: Criar uma conferência simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa0bfd8fede9fa61aedb6b630a2451803e2257d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782916"
---
# <a name="create-a-simple-conference"></a><span data-ttu-id="dd09d-104">Criar uma conferência simples</span><span class="sxs-lookup"><span data-stu-id="dd09d-104">Create a Simple Conference</span></span>

<span data-ttu-id="dd09d-105">O exemplo de código a seguir demonstra a criação de uma chamada de conferência simples.</span><span class="sxs-lookup"><span data-stu-id="dd09d-105">The following code example demonstrates the creation of a simple conference call.</span></span> <span data-ttu-id="dd09d-106">Para obter informações sobre videoconferência de multimídia de IP, consulte [sobre a reunião de conferência de telefonia IP](about-rendezvous-ip-telephony-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="dd09d-106">For information on IP multicast multimedia video conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

<span data-ttu-id="dd09d-107">Antes de usar este exemplo de código, uma chamada deve estar em andamento e você deve executar as operações em [fazer uma chamada](make-a-call.md) ou [receber uma chamada](receive-a-call.md) foi executada.</span><span class="sxs-lookup"><span data-stu-id="dd09d-107">Before using this code example, a call must be in progress, and you must perform the operations in [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) have been performed.</span></span>

> [!Note]  
> <span data-ttu-id="dd09d-108">Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.</span><span class="sxs-lookup"><span data-stu-id="dd09d-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a><span data-ttu-id="dd09d-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd09d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd09d-110">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="dd09d-110">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="dd09d-111">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="dd09d-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="dd09d-112">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="dd09d-112">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



