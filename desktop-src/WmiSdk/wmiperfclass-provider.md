---
description: A partir do Windows Vista, esse provedor cria as classes do contador de desempenho do WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Provedor de WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011122"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="504a7-103">Provedor de WmiPerfClass</span><span class="sxs-lookup"><span data-stu-id="504a7-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="504a7-104">A partir do Windows Vista, esse provedor cria as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI.</span><span class="sxs-lookup"><span data-stu-id="504a7-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="504a7-105">Os dados são fornecidos dinamicamente para essas classes de desempenho WMI pelo provedor [WMIPerfInst](wmiperfinst-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="504a7-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="504a7-106">O processo de descoberta automática/autolimpeza (ADAP) não transfere mais objetos de contador de desempenho para classes de desempenho WMI no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="504a7-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="504a7-107">Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="504a7-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="504a7-108">Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="504a7-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="504a7-109">Embora não seja recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo do [*adaptador reverso do adap*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho, a exceção é o desenvolvimento de um driver Windows Driver Model que fornece dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="504a7-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="504a7-110">Embora o processo do adaptador reverso continue a funcionar para compatibilidade com versões anteriores, o método recomendado é usar os [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="504a7-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="504a7-111">O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) desse provedor é "WmiPerfClass".</span><span class="sxs-lookup"><span data-stu-id="504a7-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="504a7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="504a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="504a7-113">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="504a7-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="504a7-114">Bibliotecas de desempenho e WMI</span><span class="sxs-lookup"><span data-stu-id="504a7-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="504a7-115">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="504a7-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
