---
title: Rastreamento de rede no Windows 7
description: O Windows 7 expande o NDF (estrutura de diagnóstico de rede) para fornecer um método rápido para solucionar problemas de conectividade de rede, habilitando a coleta de todas as informações necessárias em uma única etapa e aproveitando o ETW (rastreamento de eventos para Windows) para registrar em log os pacotes de eventos de rede em um único arquivo.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366682"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="40428-103">Rastreamento de rede no Windows 7</span><span class="sxs-lookup"><span data-stu-id="40428-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="40428-104">À medida que a complexidade da pilha de rede aumenta, muitas vezes é difícil rastrear e diagnosticar rapidamente os problemas dentro da pilha.</span><span class="sxs-lookup"><span data-stu-id="40428-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="40428-105">O Windows 7 expande o NDF (estrutura de diagnóstico de rede) para fornecer um método rápido para solucionar problemas de conectividade de rede, habilitando a coleta de todas as informações necessárias em uma única etapa e aproveitando o [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para registrar eventos de rede & pacotes em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="40428-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="40428-106">Os eventos e os pacotes relacionados são agrupados para uma determinada atividade, como navegar por um site, entre os vários componentes na pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="40428-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="40428-107">A saída desse processo é um arquivo de log de rastreamento de eventos (ETL).</span><span class="sxs-lookup"><span data-stu-id="40428-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="40428-108">Ao permitir que todos os eventos relacionados a uma atividade específica sejam exibidos ao mesmo tempo nesse arquivo, o tempo necessário para isolar e diagnosticar problemas de rede pode ser bastante reduzido.</span><span class="sxs-lookup"><span data-stu-id="40428-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40428-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="40428-109">In This Section</span></span>



| <span data-ttu-id="40428-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="40428-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40428-111">Rastreamento de rede no Windows 7: arquitetura</span><span class="sxs-lookup"><span data-stu-id="40428-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="40428-112">Ferramentas para solução de problemas usando o rastreamento de rede no Windows 7</span><span class="sxs-lookup"><span data-stu-id="40428-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="40428-113">Rastreamento de rede no Windows 7: cenários</span><span class="sxs-lookup"><span data-stu-id="40428-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 