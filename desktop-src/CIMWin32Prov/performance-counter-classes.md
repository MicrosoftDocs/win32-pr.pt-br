---
description: As classes de contador de desempenho permitem o acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826703"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="3a957-103">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="3a957-103">Performance Counter Classes</span></span>

<span data-ttu-id="3a957-104">As classes de contador de desempenho permitem o acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes.</span><span class="sxs-lookup"><span data-stu-id="3a957-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="3a957-105">Essas classes consistem em classes de contador de desempenho brutos e classes de contador de desempenho formatadas.</span><span class="sxs-lookup"><span data-stu-id="3a957-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="3a957-106">Provedores diferentes fornecem dados de biblioteca de desempenho por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="3a957-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="3a957-107">Os provedores [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) fornecem classes para os [contadores de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)da versão 1 e da versão 2.</span><span class="sxs-lookup"><span data-stu-id="3a957-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="3a957-108">Esses provedores mantêm a compatibilidade com as classes disponíveis em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="3a957-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="3a957-109">As classes nesta seção são as classes base abstratas usadas para criar classes de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="3a957-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="3a957-110">Essa não é uma lista completa de classes que você pode encontrar em seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3a957-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="3a957-111">Para obter mais informações, consulte [bibliotecas de desempenho e WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3a957-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a957-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3a957-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3a957-113">**Desempenho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3a957-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="3a957-114">A classe base para as classes de contador de desempenho [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="3a957-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="3a957-115">**\_PerfFormattedData Win32**</span><span class="sxs-lookup"><span data-stu-id="3a957-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="3a957-116">uma classe base abstrata para as classes de dados previamente instaladas, calculadas.</span><span class="sxs-lookup"><span data-stu-id="3a957-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="3a957-117">**\_PerfRawData Win32**</span><span class="sxs-lookup"><span data-stu-id="3a957-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="3a957-118">A classe base abstrata para todas as classes de contador de desempenho brutos concretos.</span><span class="sxs-lookup"><span data-stu-id="3a957-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3a957-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a957-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a957-120">Classes Win32</span><span class="sxs-lookup"><span data-stu-id="3a957-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
