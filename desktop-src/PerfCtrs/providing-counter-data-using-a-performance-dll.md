---
description: Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode gravar uma DLL de desempenho para fornecer os dados.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fornecendo dados de contador usando uma DLL de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783249"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="7a2ce-103">Fornecendo dados de contador usando uma DLL de desempenho</span><span class="sxs-lookup"><span data-stu-id="7a2ce-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a2ce-104">Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="7a2ce-105">Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método também.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="7a2ce-106">Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode gravar uma DLL de desempenho para fornecer os dados.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="7a2ce-107">Quando um consumidor consulta dados de desempenho, o sistema carrega a DLL do provedor no processo do consumidor e chama o provedor para coletar os dados.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="7a2ce-108">Para obter detalhes sobre como escrever a DLL de desempenho, consulte [criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7a2ce-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="7a2ce-109">O sistema usa o registro para determinar qual provedor deve ser chamado.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="7a2ce-110">Para obter informações sobre como registrar seu provedor e os contadores aos quais ele dá suporte, consulte [adicionando contadores de desempenho](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="7a2ce-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="7a2ce-111">Não há suporte para DLLs de desempenho no Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="7a2ce-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="7a2ce-112">Se estiver escrevendo um componente que deve ser executado no Windows OneCore, use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="7a2ce-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
