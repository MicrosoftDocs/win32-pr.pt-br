---
description: O provedor WMIPerfClass e o provedor WMIPerfInst fornecem dinamicamente dados do contador de desempenho para as classes do contador de desempenho do WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de desempenho e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765637"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="473b1-103">Bibliotecas de desempenho e WMI</span><span class="sxs-lookup"><span data-stu-id="473b1-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="473b1-104">O [provedor WMIPerfClass](wmiperfclass-provider.md) e o [provedor WMIPerfInst](wmiperfinst-provider.md) fornecem dinamicamente dados do contador de desempenho para as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI.</span><span class="sxs-lookup"><span data-stu-id="473b1-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="473b1-105">Provedores de WMIPerfClass e WMIPerfInst</span><span class="sxs-lookup"><span data-stu-id="473b1-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="473b1-106">O [provedor WMIPerfClass](wmiperfclass-provider.md) cria [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="473b1-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="473b1-107">O [provedor WMIPerfInst](wmiperfinst-provider.md) fornece dinamicamente dados do contador de desempenho para essas classes.</span><span class="sxs-lookup"><span data-stu-id="473b1-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="473b1-108">O provedor do provedor WMIPerfClass fornece classes para os [contadores de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)da versão 1 e da versão 2.</span><span class="sxs-lookup"><span data-stu-id="473b1-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="473b1-109">Os contadores da versão 1 são encontrados no registro em **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.</span><span class="sxs-lookup"><span data-stu-id="473b1-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="473b1-110">Os serviços que fornecem dados de desempenho têm uma subchave de **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="473b1-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="473b1-111">As classes de desempenho WMI criadas a partir dos contadores da versão 1 não têm "contadores" como parte do nome.</span><span class="sxs-lookup"><span data-stu-id="473b1-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="473b1-112">Os **GUIDs** que identificam um provedor de contador de desempenho versão 2 são encontrados no registro em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="473b1-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="473b1-113">WMIPerfClass é registrado como um provedor de classe WMI normal.</span><span class="sxs-lookup"><span data-stu-id="473b1-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="473b1-114">WMIPerfInst é um provedor de instância do WMI que fornece dados do PDH (auxiliar de dados de desempenho) para os contadores da versão 1 e da versão 2.</span><span class="sxs-lookup"><span data-stu-id="473b1-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="473b1-115">Para obter mais informações, consulte [usando as funções de PDH para consumir dados de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="473b1-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="473b1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="473b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="473b1-117">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="473b1-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="473b1-118">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="473b1-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
