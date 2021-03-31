---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Somente 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171984"
---
# <a name="64-bit-only"></a><span data-ttu-id="e7253-103">Somente 64 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e7253-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="e7253-104">Affected Platforms</span></span>

<span data-ttu-id="e7253-105">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7253-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="e7253-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="e7253-106">Feature Impact</span></span>

 <span data-ttu-id="e7253-107">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="e7253-107">**Severity** - Low</span></span>  
<span data-ttu-id="e7253-108">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="e7253-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="e7253-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7253-109">Description</span></span>

<span data-ttu-id="e7253-110">O Windows Server 2008 R2 é fornecido com um SKU de 64 bits apenas; nenhuma SKU de 32 bits está disponível para a versão do servidor do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e7253-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="e7253-111">No entanto, um SKU de 32 bits continua disponível para o cliente do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7253-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e7253-112">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="e7253-112">Manifestation of Impact</span></span>

<span data-ttu-id="e7253-113">Isso afetará três áreas:</span><span class="sxs-lookup"><span data-stu-id="e7253-113">This will impact three areas:</span></span>

-   <span data-ttu-id="e7253-114">drivers de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-114">32-bit drivers</span></span>
-   <span data-ttu-id="e7253-115">plug-ins de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="e7253-116">executáveis de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="e7253-117">Solução para drivers de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="e7253-118">Recompile drivers de 32 bits como drivers de 64 bits assinados.</span><span class="sxs-lookup"><span data-stu-id="e7253-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="e7253-119">Solução para plug-ins de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="e7253-120">O WoW64, um emulador x86, permite que aplicativos baseados em Windows de 32 bits sejam executados diretamente em janelas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="e7253-121">O WoW64 agora é um recurso opcional que você deve instalar se for necessário executar o código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="e7253-122">O sistema isola os aplicativos de 32 bits de aplicativos de 64 bits, o que inclui a prevenção de colisões de arquivo e registro.</span><span class="sxs-lookup"><span data-stu-id="e7253-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="e7253-123">Há suporte para aplicativos de console, GUI e serviço.</span><span class="sxs-lookup"><span data-stu-id="e7253-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="e7253-124">O sistema fornece interoperabilidade entre o limite de 32/64 para cenários como recortar e colar e COM.</span><span class="sxs-lookup"><span data-stu-id="e7253-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="e7253-125">No entanto, os processos de 32 bits não podem carregar DLLs de 64 bits e os processos de 64 bits não podem carregar DLLs de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="e7253-126">Normalmente vemos isso nos plug-ins do Shell escritos para o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7253-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="e7253-127">Um aplicativo de 32 bits pode detectar se ele está em execução no WOW64 chamando a função IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="e7253-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="e7253-128">O aplicativo pode obter informações adicionais sobre o processador usando a função GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="e7253-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="e7253-129">Observe que o Windows de 64 bits não oferece suporte à execução de aplicativos baseados no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="e7253-130">O principal motivo é que os identificadores têm 32 bits significativos no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="e7253-131">Portanto, os identificadores não podem ser truncados e passados para aplicativos de 16 bits sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="e7253-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="e7253-132">As tentativas de iniciar aplicativos de 16 bits falham com o seguinte erro: erro de \_ \_ formato exe inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="e7253-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="e7253-133">Solução para executáveis de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="e7253-134">o Windows de 64 bits reconhece um número limitado de programas de instalação de 16 bits específicos e substitui uma versão de 32 bits portada.</span><span class="sxs-lookup"><span data-stu-id="e7253-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="e7253-135">A lista de substituições é armazenada no registro na seguinte chave: HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 há suporte interno para vários mecanismos de instalação, incluindo instaladores do InstallShield 5. x.</span><span class="sxs-lookup"><span data-stu-id="e7253-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="e7253-136">Observe que o Windows Installer de 64 bits pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e7253-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e7253-137">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="e7253-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="e7253-138">Executando aplicativos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="e7253-139">Desempenho e consumo de memória</span><span class="sxs-lookup"><span data-stu-id="e7253-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="e7253-140">Detalhes da implementação do WOW64</span><span class="sxs-lookup"><span data-stu-id="e7253-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="e7253-141">Redirecionador de registro</span><span class="sxs-lookup"><span data-stu-id="e7253-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="e7253-142">Redirecionador do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="e7253-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="e7253-143">Gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="e7253-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="e7253-144">Afinidade do Processador</span><span class="sxs-lookup"><span data-stu-id="e7253-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="e7253-145">Comunicação entre processos</span><span class="sxs-lookup"><span data-stu-id="e7253-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="e7253-146">Instalação de aplicativos em sistemas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="e7253-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="e7253-147">Depurando WOW64</span><span class="sxs-lookup"><span data-stu-id="e7253-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="e7253-148">**Função IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="e7253-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="e7253-149">**Função GetNativeSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="e7253-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
