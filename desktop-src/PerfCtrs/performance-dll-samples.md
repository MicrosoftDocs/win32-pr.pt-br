---
description: O SDK do Windows (WSDK) contém três DLLs de desempenho de exemplo completas.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Amostras de DLL de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783250"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="dcf66-103">Amostras de DLL de desempenho</span><span class="sxs-lookup"><span data-stu-id="dcf66-103">Performance DLL Samples</span></span>

<span data-ttu-id="dcf66-104">O SDK do Windows (WSDK) contém três DLLs de desempenho de exemplo completas.</span><span class="sxs-lookup"><span data-stu-id="dcf66-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="dcf66-105">Esses exemplos estão localizados no diretório Samples \\ WinBase \\ WinNT \\ PerfTool \\ PerfDlls.</span><span class="sxs-lookup"><span data-stu-id="dcf66-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="dcf66-106">A raiz desse caminho é o diretório de instalação base do WSDK.</span><span class="sxs-lookup"><span data-stu-id="dcf66-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="dcf66-107">Você pode baixar o WSDK do [SDK (Software Development Kit) do Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (pesquise por SDK do Windows e selecione o download para o sistema operacional mais recente).</span><span class="sxs-lookup"><span data-stu-id="dcf66-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="dcf66-108">Os exemplos contidos neste diretório são:</span><span class="sxs-lookup"><span data-stu-id="dcf66-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="dcf66-109">**AppMem**— fornece contrapartes das funções [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que relatam informações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dcf66-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="dcf66-110">Os contadores de desempenho no registro e a ferramenta de desempenho podem ler as informações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dcf66-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="dcf66-111">**LeakyBin**– demonstra o uso de contadores de desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcf66-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="dcf66-112">**PerfGen**— fornece três ondas em cinco períodos diferentes para uso com a ferramenta de desempenho para fornecer dados a uma taxa e um valor conhecidos.</span><span class="sxs-lookup"><span data-stu-id="dcf66-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="dcf66-113">Isso pode ser útil em aplicativos de teste que usam dados de desempenho e precisam de valores previsíveis para teste.</span><span class="sxs-lookup"><span data-stu-id="dcf66-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
