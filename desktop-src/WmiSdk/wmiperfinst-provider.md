---
description: A partir do Windows Vista, o provedor WmiPerfInst fornece dados de contador de desempenho brutos e formatados dinamicamente para classes de contador de desempenho WMI derivadas do desempenho do Win32 \_ .
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Provedor de WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770632"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="86dcb-103">Provedor de WmiPerfInst</span><span class="sxs-lookup"><span data-stu-id="86dcb-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="86dcb-104">A partir do Windows Vista, o provedor WmiPerfInst fornece dados de contador de desempenho brutos e formatados dinamicamente para [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivadas do [**\_ desempenho do Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="86dcb-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="86dcb-105">Esse provedor substitui o [provedor de dados de desempenho formatado](formatted-performance-data-provider.md), também conhecido como "provedor de contador de cooked", e o [provedor de contador de desempenho](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="86dcb-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="86dcb-106">O provedor WmiPerfInst fornece dados para as classes WMI que são fornecidas pelo provedor [WMIPerfClass](wmiperfclass-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="86dcb-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="86dcb-107">Esse provedor é uma ponte entre instâncias de PDH (auxiliar de dados de desempenho) e as classes de desempenho do WMI fornecidas pelo provedor WmiPerfClass.</span><span class="sxs-lookup"><span data-stu-id="86dcb-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="86dcb-108">Quando o WmiPerfInst recebe uma consulta de dados, ele carrega a classe e usa os [qualificadores](qualifiers-specific-to-wmi-performance-classes.md) de classe e propriedade para localizar as instâncias de PDH.</span><span class="sxs-lookup"><span data-stu-id="86dcb-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="86dcb-109">Para obter mais informações, consulte [usando as funções de PDH para consumir dados de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="86dcb-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="86dcb-110">Não é recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo do [*adaptador inverso do adap*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="86dcb-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="86dcb-111">A exceção é quando você está desenvolvendo um driver de Windows Driver Model e deseja fornecer dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="86dcb-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="86dcb-112">Embora o processo do adaptador reverso continue a funcionar para compatibilidade com versões anteriores, o método recomendado é usar os [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="86dcb-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="86dcb-113">O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) desse provedor é "WmiPerfInst".</span><span class="sxs-lookup"><span data-stu-id="86dcb-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="86dcb-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86dcb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86dcb-115">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="86dcb-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="86dcb-116">Bibliotecas de desempenho e WMI</span><span class="sxs-lookup"><span data-stu-id="86dcb-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="86dcb-117">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="86dcb-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
