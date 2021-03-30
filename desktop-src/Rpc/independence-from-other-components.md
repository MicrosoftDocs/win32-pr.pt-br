---
title: Independência de outros componentes
description: Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo pelo qual a cadeia passada não reconhece dados de erro estendidos ou não aproveita isso. As abordagens recomendadas para essas situações são fornecidas no final desta seção.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independência de outros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916561"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="6684d-105">Independência de outros componentes</span><span class="sxs-lookup"><span data-stu-id="6684d-105">Independence From Other Components</span></span>

<span data-ttu-id="6684d-106">Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo pelo qual a cadeia passada não reconhece dados de erro estendidos ou não aproveita isso.</span><span class="sxs-lookup"><span data-stu-id="6684d-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="6684d-107">As abordagens recomendadas para essas situações são fornecidas no final desta seção.</span><span class="sxs-lookup"><span data-stu-id="6684d-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="6684d-108">Os dados de erro estendidos são mais úteis quando aplicativos ou servidores que usam RPC aproveitam as informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="6684d-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="6684d-109">Ao investigar um \_ código de erro RPC S \_ \* e os servidores ou aplicativos envolvidos não disponibilizarem dados de erro estendidos, considere as seguintes abordagens:</span><span class="sxs-lookup"><span data-stu-id="6684d-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="6684d-110">Faça uma detecção.</span><span class="sxs-lookup"><span data-stu-id="6684d-110">Take a sniff.</span></span>

    <span data-ttu-id="6684d-111">Reproduza o cenário ao fazer a detecção.</span><span class="sxs-lookup"><span data-stu-id="6684d-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="6684d-112">A detecção da transmissão conterá os dados de erro estendidos.</span><span class="sxs-lookup"><span data-stu-id="6684d-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="6684d-113">Examine-o no depurador.</span><span class="sxs-lookup"><span data-stu-id="6684d-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="6684d-114">Se um farejamento do problema não funcionar, porque a chamada é local ou porque o erro é originado localmente, anexe um depurador ao processo que retorna o erro e coloque um ponto de interrupção imediatamente após a chamada RPC gerar o erro.</span><span class="sxs-lookup"><span data-stu-id="6684d-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="6684d-115">O RPC geralmente indica erros lançando exceções, portanto, se você estiver procurando o erro 1825 ( \_ erro de pacote RPC s s \_ \_ \_ ), habilite a exceção 1825 e quando o depurador interromper essa exceção, examine as informações de erro estendidas para o thread.</span><span class="sxs-lookup"><span data-stu-id="6684d-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




