---
description: Não é recomendável escrever um provedor WMI de alto desempenho para criar contadores de desempenho.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Criando um provedor de instância em um provedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789221"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="90d89-103">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="90d89-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="90d89-104">Não é recomendável escrever um provedor WMI de alto desempenho para criar contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="90d89-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="90d89-105">A partir do Windows Vista, as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI não são mais migradas para as bibliotecas de desempenho do Windows pelo adaptador reverso de autodescoberta/autolimpeza (ADAP).</span><span class="sxs-lookup"><span data-stu-id="90d89-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="90d89-106">Para criar um provedor de contador de desempenho, use [contadores de desempenho versão 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="90d89-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="90d89-107">Depois que os objetos de biblioteca de desempenho são criados, o [provedor WMIPerfClass](wmiperfclass-provider.md) analisa os objetos e cria ou atualiza uma classe WMI derivada [**do \_ desempenho do Win32**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de desempenho.</span><span class="sxs-lookup"><span data-stu-id="90d89-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="90d89-108">O [provedor WMIPerfInst](wmiperfinst-provider.md) , em seguida, fornece dinamicamente dados de contador de desempenho brutos e formatados para as classes de desempenho WMI.</span><span class="sxs-lookup"><span data-stu-id="90d89-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="90d89-109">O procedimento de alto nível a seguir fornece as etapas necessárias para criar um provedor de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="90d89-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="90d89-110">**Para criar um provedor de alto desempenho**</span><span class="sxs-lookup"><span data-stu-id="90d89-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="90d89-111">Registre seu provedor com o WMI.</span><span class="sxs-lookup"><span data-stu-id="90d89-111">Register your provider with WMI.</span></span> <span data-ttu-id="90d89-112">Para obter mais informações, consulte [registrando um provedor de High-Performance](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90d89-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="90d89-113">Implemente seu provedor.</span><span class="sxs-lookup"><span data-stu-id="90d89-113">Implement your provider.</span></span> <span data-ttu-id="90d89-114">Para obter mais informações, consulte [escrevendo um provedor de instância](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90d89-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="90d89-115">Implemente a interface de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="90d89-115">Implement the high-performance interface.</span></span> <span data-ttu-id="90d89-116">Para obter mais informações, consulte [implementando a Interface High-Performance](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="90d89-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="90d89-117">Derive e escreva seu esquema de formato MOF (MOF) para obter dados brutos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="90d89-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="90d89-118">Para obter mais informações, consulte [dando suporte à \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="90d89-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="90d89-119">Derive e grave seu esquema MOF para obter dados pré-calculados.</span><span class="sxs-lookup"><span data-stu-id="90d89-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="90d89-120">Ao dar suporte a essa classe, o provedor não precisa executar os cálculos.</span><span class="sxs-lookup"><span data-stu-id="90d89-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="90d89-121">Esses dados serão os mesmos que aparecem no monitor do sistema no perfmon.</span><span class="sxs-lookup"><span data-stu-id="90d89-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="90d89-122">Para obter mais informações, consulte [dando suporte à \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="90d89-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90d89-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90d89-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d89-124">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="90d89-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="90d89-125">Bibliotecas de desempenho e WMI</span><span class="sxs-lookup"><span data-stu-id="90d89-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
