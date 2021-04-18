---
description: No Windows Vista, os contadores de desempenho implementaram uma nova arquitetura (versão 2,0) para fornecer dados do contador.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fornecendo dados do contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764630"
---
# <a name="providing-counter-data"></a><span data-ttu-id="ae489-103">Fornecendo dados do contador</span><span class="sxs-lookup"><span data-stu-id="ae489-103">Providing Counter Data</span></span>

<span data-ttu-id="ae489-104">Componentes de software que publicam dados por meio de contadores de desempenho do Windows são chamados de provedores de dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae489-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="ae489-105">O Windows dá suporte a dois tipos de provedores de dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae489-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="ae489-106">Os provedores de dados de desempenho herdados (**provedores v1**) são implementados usando um. Arquivo INI e uma DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae489-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="ae489-107">Os provedores de dados de desempenho modernos (**provedores v2**) usam um. O MAN (manifesto XML) e as APIs do provedor do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae489-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="ae489-108">Manifestos</span><span class="sxs-lookup"><span data-stu-id="ae489-108">Manifests</span></span>

<span data-ttu-id="ae489-109">Os provedores de dados de desempenho modernos usam um. MAN (manifesto XML) para definir os dados do contador e usar as APIs do provedor do contador de desempenho para gerenciar dados no contexto do provedor.</span><span class="sxs-lookup"><span data-stu-id="ae489-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="ae489-110">Provedores implementados usando um manifesto e APIs de provedor de contador de desempenho geralmente são chamados de **provedores v2**.</span><span class="sxs-lookup"><span data-stu-id="ae489-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="ae489-111">O Windows dá suporte a provedores v2 de modo de usuário no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae489-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="ae489-112">Para obter detalhes do modo de usuário, consulte [fornecendo dados do contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="ae489-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="ae489-113">O Windows dá suporte a provedores v2 do modo kernel no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae489-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="ae489-114">Para obter detalhes do modo kernel, consulte [monitoramento de desempenho do modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ae489-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="ae489-115">DLL de desempenho (preterida)</span><span class="sxs-lookup"><span data-stu-id="ae489-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="ae489-116">Na arquitetura do contador de desempenho herdado, os provedores implementaram uma DLL de desempenho que foi executada no processo do consumidor para coletar e fornecer os dados do contador quando um consumidor o solicitou.</span><span class="sxs-lookup"><span data-stu-id="ae489-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="ae489-117">O provedor usou uma inicialização (. INI) e as entradas do registro para definir os contadores e configurar a DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae489-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="ae489-118">Provedores implementados usando um. O arquivo INI e uma DLL de desempenho geralmente são chamados de **provedores v1**.</span><span class="sxs-lookup"><span data-stu-id="ae489-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="ae489-119">Embora você ainda possa usar uma DLL de desempenho para fornecer dados de contador, essa arquitetura é preterida devido a limitações significativas de desempenho e confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="ae489-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="ae489-120">Além disso, os provedores v1 costumam ser mais difíceis de implementar, pois exigem o envio de uma DLL separada que deve ser executada no processo do consumidor.</span><span class="sxs-lookup"><span data-stu-id="ae489-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="ae489-121">Para obter detalhes, consulte [fornecendo dados do contador usando uma DLL de desempenho](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="ae489-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
