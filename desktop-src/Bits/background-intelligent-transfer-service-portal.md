---
title: BITS
description: O BITS (Serviço de Transferência Inteligente em Segundo Plano) transfere arquivos (downloads ou uploads) entre um cliente e um servidor e fornece informações de progresso relacionadas às transferências.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- BITS
- Serviço de Transferência Inteligente em Segundo Plano, página inicial
- BITS (consulte Serviço de Transferência Inteligente em Segundo Plano)
- baixando arquivos BITS
- BITS de transferência de arquivo em segundo plano
- carregando BITS de arquivos
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424206"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="2ec25-109">BITS</span><span class="sxs-lookup"><span data-stu-id="2ec25-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="2ec25-110">Finalidade</span><span class="sxs-lookup"><span data-stu-id="2ec25-110">Purpose</span></span>

<span data-ttu-id="2ec25-111">Serviço de Transferência Inteligente em Segundo Plano (BITS) é usado por programadores e administradores de sistema para baixar arquivos de ou carregar arquivos para servidores Web HTTP e compartilhamentos de arquivos SMB.</span><span class="sxs-lookup"><span data-stu-id="2ec25-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="2ec25-112">O BITS levará o custo da transferência em consideração, bem como o uso da rede para que o trabalho em primeiro plano do usuário tenha o menor impacto possível.</span><span class="sxs-lookup"><span data-stu-id="2ec25-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="2ec25-113">O BITS também lida com interuptions de rede, pausando e retomando transferências automaticamente, mesmo após uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="2ec25-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="2ec25-114">O BITS inclui cmdlets do PowerShell para criar e gerenciar transferências, bem como o utilitário de linha de comando BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="2ec25-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="2ec25-115">O BITS pode ser usado pelo Windows para baixar atualizações para seu sistema local.</span><span class="sxs-lookup"><span data-stu-id="2ec25-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="2ec25-116">Se você for um usuário final pesquisando maneiras de solucionar problemas de instalação do BITS, consulte [corrigir problemas de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="2ec25-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="2ec25-117">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="2ec25-117">Where applicable</span></span>

<span data-ttu-id="2ec25-118">Use o BITS para aplicativos que precisam:</span><span class="sxs-lookup"><span data-stu-id="2ec25-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="2ec25-119">Baixar de ou carregar arquivos para um servidor Web ou servidor de arquivos SMB de HTTP ou REST.</span><span class="sxs-lookup"><span data-stu-id="2ec25-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="2ec25-120">Retome automaticamente as transferências de arquivos após a desconexão da rede e a reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="2ec25-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="2ec25-121">Preserve a capacidade de resposta de outros aplicativos de rede.</span><span class="sxs-lookup"><span data-stu-id="2ec25-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="2ec25-122">Lembre-se do custo de rede em como, por exemplo, redes móveis</span><span class="sxs-lookup"><span data-stu-id="2ec25-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="2ec25-123">Opcionalmente, trabalhar com o [BranchCache](/windows-server/networking/branchcache/branchcache) para otimizar o tráfego de WAN (rede de longa distância)</span><span class="sxs-lookup"><span data-stu-id="2ec25-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2ec25-124">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="2ec25-124">Developer audience</span></span>

<span data-ttu-id="2ec25-125">O BITS é uma interface COM criada para desenvolvedores C e C++ que também podem ser usados por desenvolvedores do .NET.</span><span class="sxs-lookup"><span data-stu-id="2ec25-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="2ec25-126">Os desenvolvedores de UWP devem usar a API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e não a API bits.</span><span class="sxs-lookup"><span data-stu-id="2ec25-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="2ec25-127">Versões do BITS</span><span class="sxs-lookup"><span data-stu-id="2ec25-127">BITS versions</span></span>

<span data-ttu-id="2ec25-128">Para obter o histórico completo de versões e informações sobre o sistema operacional anterior, consulte [Novidades.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="2ec25-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="2ec25-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2ec25-129">In this section</span></span>



| <span data-ttu-id="2ec25-130">Tópico</span><span class="sxs-lookup"><span data-stu-id="2ec25-130">Topic</span></span>                                                           | <span data-ttu-id="2ec25-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ec25-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ec25-132">Sobre BITS</span><span class="sxs-lookup"><span data-stu-id="2ec25-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="2ec25-133">Informações gerais sobre BITS.</span><span class="sxs-lookup"><span data-stu-id="2ec25-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="2ec25-134">Usando BITS</span><span class="sxs-lookup"><span data-stu-id="2ec25-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="2ec25-135">Guia de procedimento para desenvolver clientes BITS que transferem arquivos entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="2ec25-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="2ec25-136">Referência BITS</span><span class="sxs-lookup"><span data-stu-id="2ec25-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="2ec25-137">Informações de referência para as interfaces de programação BITS.</span><span class="sxs-lookup"><span data-stu-id="2ec25-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="2ec25-138">Também contém informações sobre exemplos, ferramentas, configurações de servidor para trabalhos de upload e o protocolo de upload.</span><span class="sxs-lookup"><span data-stu-id="2ec25-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="2ec25-139">Práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="2ec25-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="2ec25-140">Informações a considerar ao criar um aplicativo que usa BITS.</span><span class="sxs-lookup"><span data-stu-id="2ec25-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="2ec25-141">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2ec25-141">Additional resources</span></span>

<span data-ttu-id="2ec25-142">A seguir estão recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="2ec25-142">The following are additional resources.</span></span>


|    <span data-ttu-id="2ec25-143">Recurso</span><span class="sxs-lookup"><span data-stu-id="2ec25-143">Resource</span></span>         |    <span data-ttu-id="2ec25-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ec25-144">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec25-145">DLL de referência do .NET</span><span class="sxs-lookup"><span data-stu-id="2ec25-145">.NET Reference DLL</span></span>   | <span data-ttu-id="2ec25-146">Para obter informações sobre como usar o BITS do .NET usando DLLs de referência, consulte Chamando bits do [.NET usando DLLs de referência](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="2ec25-146">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="2ec25-147">Wrapper do .NET</span><span class="sxs-lookup"><span data-stu-id="2ec25-147">.NET Wrapper</span></span>   | <span data-ttu-id="2ec25-148">Para outros wrappers do .NET para BITS, você pode pesquisar [projetos marcados](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) no nuget com a marca BITS.</span><span class="sxs-lookup"><span data-stu-id="2ec25-148">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

