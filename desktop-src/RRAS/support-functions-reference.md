---
title: Referência de funções de suporte
description: As funções a seguir são fornecidas para protocolos de roteamento pelo Gerenciador de roteador.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Interface do protocolo de roteamento RRAS, funções de suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454239"
---
# <a name="support-functions-reference"></a><span data-ttu-id="51ac6-104">Referência de funções de suporte</span><span class="sxs-lookup"><span data-stu-id="51ac6-104">Support Functions Reference</span></span>

<span data-ttu-id="51ac6-105">As funções a seguir são fornecidas para protocolos de roteamento pelo Gerenciador de roteador.</span><span class="sxs-lookup"><span data-stu-id="51ac6-105">The following functions are provided to routing protocols by the router manager.</span></span> <span data-ttu-id="51ac6-106">Quando o Gerenciador de roteador chama a função [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementada pelo protocolo de roteamento), o Gerenciador de roteador passa o protocolo de roteamento a uma estrutura de [**\_ funções de suporte**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) que contém ponteiros para essas funções:</span><span class="sxs-lookup"><span data-stu-id="51ac6-106">When the router manager calls the [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) function (implemented by the routing protocol), the router manager passes the routing protocol a [**SUPPORT\_FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) structure containing pointers to these functions:</span></span>

<span data-ttu-id="51ac6-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span></span>

<span data-ttu-id="51ac6-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span></span>

<span data-ttu-id="51ac6-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span></span>

<span data-ttu-id="51ac6-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span></span>

<span data-ttu-id="51ac6-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span></span>

<span data-ttu-id="51ac6-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span></span>

<span data-ttu-id="51ac6-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span></span>

<span data-ttu-id="51ac6-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span></span>

<span data-ttu-id="51ac6-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51ac6-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span></span>

 

 