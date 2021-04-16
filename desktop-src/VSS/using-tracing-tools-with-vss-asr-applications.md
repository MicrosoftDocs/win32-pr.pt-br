---
description: Você pode usar a ferramenta logman para coletar informações de rastreamento para aplicativos VSS que usam a recuperação automatizada do sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Usando ferramentas de rastreamento com aplicativos ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794551"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="ec1ef-103">Usando ferramentas de rastreamento com aplicativos ASR</span><span class="sxs-lookup"><span data-stu-id="ec1ef-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="ec1ef-104">Você pode usar a ferramenta logman para coletar informações de rastreamento para aplicativos VSS que usam a [recuperação automatizada do sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="ec1ef-105">Logman (logman.exe) é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="ec1ef-106">Ele está incluído no Windows XP e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ec1ef-107">Ou, se preferir, você pode usar a ferramenta tracelog para coletar as mesmas informações de rastreamento de ASR.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="ec1ef-108">O tracelog está incluído no Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="ec1ef-109">Para usar as ferramentas de rastreamento com o VSS, consulte [usando ferramentas de rastreamento com o VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="ec1ef-110">Usando logman</span><span class="sxs-lookup"><span data-stu-id="ec1ef-110">Using Logman</span></span>

<span data-ttu-id="ec1ef-111">O procedimento a seguir descreve como usar o logman com seu aplicativo ASR.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="ec1ef-112">**Para usar logman com seu aplicativo ASR**</span><span class="sxs-lookup"><span data-stu-id="ec1ef-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="ec1ef-113">Use o seguinte comando para iniciar o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="ec1ef-114">**logman start ASR-o** *x: \\ \* \* \* ASR. etl-ETS-p {6407345b-94F2-44c8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="ec1ef-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="ec1ef-115">Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="ec1ef-116">Para obter o melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="ec1ef-117">Use o seguinte comando para interromper o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="ec1ef-118">**logman Stop ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="ec1ef-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="ec1ef-119">O arquivo de log de rastreamento é *x: \\* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="ec1ef-120">Para obter mais informações sobre a ferramenta Logman, consulte [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="ec1ef-121">Usando tracelog</span><span class="sxs-lookup"><span data-stu-id="ec1ef-121">Using Tracelog</span></span>

<span data-ttu-id="ec1ef-122">O procedimento a seguir descreve como usar o tracelog.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="ec1ef-123">**Para usar o tracelog**</span><span class="sxs-lookup"><span data-stu-id="ec1ef-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="ec1ef-124">Crie um arquivo de texto chamado ASR. CTL que contenha apenas o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="ec1ef-125">**6407345b-94F2-44c8-b3db-4e076be46816 ASR**</span><span class="sxs-lookup"><span data-stu-id="ec1ef-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="ec1ef-126">Use o seguinte comando para iniciar o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="ec1ef-127">**tracelog-iniciar ASR-f** *x: \\ \* \* \* ASR. etl-GUID ASR. CTL-Flag* 0xFF\*</span><span class="sxs-lookup"><span data-stu-id="ec1ef-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="ec1ef-128">Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="ec1ef-129">Para obter o melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="ec1ef-130">Use o seguinte comando para interromper o rastreamento:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="ec1ef-131">**tracelog-parar ASR**</span><span class="sxs-lookup"><span data-stu-id="ec1ef-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="ec1ef-132">O arquivo de log de rastreamento é *x: \\* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="ec1ef-133">Para obter mais informações sobre a ferramenta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
