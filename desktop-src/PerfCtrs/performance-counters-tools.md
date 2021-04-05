---
description: A tabela a seguir lista os
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Ferramentas de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921729"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="a2937-103">Ferramentas de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="a2937-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="a2937-104">Ferramentas de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="a2937-104">Data collection tools</span></span>

<span data-ttu-id="a2937-105">As ferramentas a seguir são úteis ao consumir ou manipular dados do contador de desempenho do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2937-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="a2937-106">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="a2937-106">Tool</span></span>|<span data-ttu-id="a2937-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2937-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="a2937-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="a2937-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="a2937-109">Ferramenta de GUI para coletar e exibir dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a2937-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="a2937-110">`perfmon.exe` inicia o MMC com o snap-in Monitor de desempenho, que fornece acesso ao monitor de desempenho, conjuntos de coletores de dados e ferramentas de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a2937-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="a2937-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="a2937-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="a2937-112">Ferramenta de linha de comando para coletar e imprimir dados do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a2937-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="a2937-113">Pode ser usado para listar os conjuntos de linhas disponíveis, listar os contadores disponíveis, imprimir dados do contador no console ou coletar dados do contador para um arquivo de log (CSV, TDF, BLG).</span><span class="sxs-lookup"><span data-stu-id="a2937-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="a2937-114">Relog</span><span class="sxs-lookup"><span data-stu-id="a2937-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="a2937-115">Ferramenta de linha de comando para transformar e mesclar arquivos de log (CSV, TDF, BLG) capturados via `typeperf.exe` ou por meio das `PDH.dll` APIs.</span><span class="sxs-lookup"><span data-stu-id="a2937-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="a2937-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="a2937-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="a2937-117">Ferramenta de linha de comando para controlar conjuntos de coletores de dados.</span><span class="sxs-lookup"><span data-stu-id="a2937-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="a2937-118">Ferramentas de provedor de dados</span><span class="sxs-lookup"><span data-stu-id="a2937-118">Data provider tools</span></span>

<span data-ttu-id="a2937-119">As ferramentas a seguir são úteis ao publicar dados do contador de desempenho do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2937-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="a2937-120">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="a2937-120">Tool</span></span>|<span data-ttu-id="a2937-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2937-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="a2937-122">CtrPP</span><span class="sxs-lookup"><span data-stu-id="a2937-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="a2937-123">Ferramenta de criação de linha de comando do SDK do Windows que valida e compila seu manifesto de provedor de contadores de desempenho v2.</span><span class="sxs-lookup"><span data-stu-id="a2937-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="a2937-124">Essa ferramenta gera os `.h` cabeçalhos e os `.rc` scripts de recursos necessários para criar um provedor v2.</span><span class="sxs-lookup"><span data-stu-id="a2937-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="a2937-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="a2937-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="a2937-126">Ferramenta de linha de comando usada para instalar seu provedor em um sistema.</span><span class="sxs-lookup"><span data-stu-id="a2937-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="a2937-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="a2937-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="a2937-128">Ferramenta de linha de comando usada para desinstalar seu provedor de um sistema.</span><span class="sxs-lookup"><span data-stu-id="a2937-128">Command-line tool used to uninstall your provider from a system.</span></span>
