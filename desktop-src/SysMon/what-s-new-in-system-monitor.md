---
title: O que há de novo no monitor do sistema
description: A tabela a seguir identifica o que há de novo para cada versão do monitor do sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2020
ms.locfileid: "104365678"
---
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="19e84-103">O que há de novo no monitor do sistema</span><span class="sxs-lookup"><span data-stu-id="19e84-103">What's New in System Monitor</span></span>

<span data-ttu-id="19e84-104">A tabela a seguir identifica o que há de novo para cada versão do monitor do sistema (SYSMON).</span><span class="sxs-lookup"><span data-stu-id="19e84-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="19e84-105">Versão</span><span class="sxs-lookup"><span data-stu-id="19e84-105">Version</span></span>     | <span data-ttu-id="19e84-106">Descrição dos recursos</span><span class="sxs-lookup"><span data-stu-id="19e84-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e84-107">Versão 3,7</span><span class="sxs-lookup"><span data-stu-id="19e84-107">Version 3.7</span></span> | <span data-ttu-id="19e84-108">Essa versão adiciona novos tipos de grafo, a capacidade de selecionar vários contadores, recuperar valores de contador de um ponto no grafo, salvar valores de contador grafado em um arquivo de log e a opção de ter um grafo de linha rolando continuamente na janela do grafo em vez de encapsular sozinho. Incluído no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="19e84-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="19e84-109">Versão 3,7</span><span class="sxs-lookup"><span data-stu-id="19e84-109">Version 3.7</span></span>

<span data-ttu-id="19e84-110">Novas propriedades e métodos que foram adicionados ao [**MYITEM**](counteritem.md).</span><span class="sxs-lookup"><span data-stu-id="19e84-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="19e84-111">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="19e84-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="19e84-112">**Selected**</span><span class="sxs-lookup"><span data-stu-id="19e84-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="19e84-113">**Visible**</span><span class="sxs-lookup"><span data-stu-id="19e84-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="19e84-114">Intervalo de valores válidos alterado para [ **MyItem. Width**](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="19e84-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="19e84-115">Novas propriedades e métodos que foram adicionados a [**SystemMonitor**](systemmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="19e84-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="19e84-116">**BatchingLock**</span><span class="sxs-lookup"><span data-stu-id="19e84-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="19e84-117">**ChartScroll**</span><span class="sxs-lookup"><span data-stu-id="19e84-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="19e84-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="19e84-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="19e84-119">**DataPointCount**</span><span class="sxs-lookup"><span data-stu-id="19e84-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="19e84-120">**EnableDigitGrouping**</span><span class="sxs-lookup"><span data-stu-id="19e84-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="19e84-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="19e84-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="19e84-122">**GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="19e84-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="19e84-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="19e84-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="19e84-124">**LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="19e84-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="19e84-125">**LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="19e84-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="19e84-126">**Relog**</span><span class="sxs-lookup"><span data-stu-id="19e84-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="19e84-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="19e84-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="19e84-128">**ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="19e84-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="19e84-129">**SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="19e84-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="19e84-130">**ShowTimeAxisLables**</span><span class="sxs-lookup"><span data-stu-id="19e84-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="19e84-131">Novas enumerações que foram adicionadas.</span><span class="sxs-lookup"><span data-stu-id="19e84-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="19e84-132">**SysmonDataType**</span><span class="sxs-lookup"><span data-stu-id="19e84-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="19e84-133">**SysmonFileType**</span><span class="sxs-lookup"><span data-stu-id="19e84-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="19e84-134">Novos valores de tipo de exibição foram adicionados a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="19e84-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





