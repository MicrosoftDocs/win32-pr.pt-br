---
title: Visão geral do Gerenciador de download
description: Visão geral do Gerenciador de download
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, download em tempo real
- lojas online, download em tempo real
- Digite 2 lojas online, download em tempo real
- Lojas online do Windows Media Player, download em segundo plano
- lojas online, download em segundo plano
- tipo 2 lojas online, download em segundo plano
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Download em tempo real
- Download em segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006063"
---
# <a name="download-manager-overview"></a><span data-ttu-id="c680d-117">Visão geral do Gerenciador de download</span><span class="sxs-lookup"><span data-stu-id="c680d-117">Download Manager Overview</span></span>

<span data-ttu-id="c680d-118">O Microsoft Windows Media Player fornece painéis de tarefas da loja online que contêm uma janela do navegador hospedado.</span><span class="sxs-lookup"><span data-stu-id="c680d-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="c680d-119">Por meio das lojas online, os usuários podem interagir com páginas da Web da loja online na Internet.</span><span class="sxs-lookup"><span data-stu-id="c680d-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="c680d-120">O Gerenciador de download do Windows Media Player fornece um modelo de objeto que você pode usar para lidar com as tarefas associadas ao download de conteúdo no computador do usuário do Microsoft Serviços de Informações da Internet (IIS) usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="c680d-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="c680d-121">Com o Gerenciador de download, você pode:</span><span class="sxs-lookup"><span data-stu-id="c680d-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="c680d-122">Gerencie vários downloads simultaneamente como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c680d-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="c680d-123">Especifique uma URL para um arquivo e inicie o download usando HTTP.</span><span class="sxs-lookup"><span data-stu-id="c680d-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="c680d-124">Consulte o estado e o progresso do download.</span><span class="sxs-lookup"><span data-stu-id="c680d-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="c680d-125">Pausar, retomar ou cancelar um download.</span><span class="sxs-lookup"><span data-stu-id="c680d-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="c680d-126">Especifique se um download ocorre em segundo plano ou em tempo real.</span><span class="sxs-lookup"><span data-stu-id="c680d-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="c680d-127">(O download em segundo plano só está disponível no sistema operacional Microsoft Windows XP.) Consulte [sobre o download em segundo plano e em tempo real](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="c680d-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="c680d-128">Especifique como o conteúdo é exibido na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c680d-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="c680d-129">Consulte [sobre a integração da biblioteca](#about-library-integration).</span><span class="sxs-lookup"><span data-stu-id="c680d-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="c680d-130">O Gerenciador de download é a solução para baixar conteúdo do código de script em páginas da Web hospedadas.</span><span class="sxs-lookup"><span data-stu-id="c680d-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="c680d-131">Para baixar conteúdo usando código C++, use o Windows XP Serviço de Transferência Inteligente em Segundo Plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="c680d-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="c680d-132">Para obter mais informações, consulte [bits](bits.md).</span><span class="sxs-lookup"><span data-stu-id="c680d-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="c680d-133">Sobre o download em segundo plano e em tempo real</span><span class="sxs-lookup"><span data-stu-id="c680d-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="c680d-134">O Gerenciador de download oferece dois tipos de download: em segundo plano e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="c680d-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="c680d-135">O tipo que você usa cabe a você, e é possível permitir que o usuário selecione o tipo de download também.</span><span class="sxs-lookup"><span data-stu-id="c680d-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="c680d-136">Se você optar por permitir que o usuário selecione o tipo de download, certifique-se de explicar as diferenças entre os dois tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c680d-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="c680d-137">O download em tempo real ocorre de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="c680d-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="c680d-138">Quando o usuário inicia um download de arquivo, todo o arquivo é transferido para o computador do usuário em um fluxo único e contínuo.</span><span class="sxs-lookup"><span data-stu-id="c680d-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="c680d-139">O usuário não pode pausar ou, de outra forma, interromper o download.</span><span class="sxs-lookup"><span data-stu-id="c680d-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="c680d-140">Se o usuário optar por fechar o Windows Media Player antes de o download ser concluído, ele perderá todos os arquivos incompletos e deverá baixá-los desde o início até a aquisição do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c680d-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="c680d-141">A principal vantagem do download em tempo real é que ele permite que o usuário adquira o conteúdo mais rápido do que o download em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c680d-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="c680d-142">O download em tempo real está disponível para usuários do Windows XP, mas é o único tipo de download disponível em versões do sistema operacional Windows antes do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c680d-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="c680d-143">O download em segundo plano ocorre de maneira gradual.</span><span class="sxs-lookup"><span data-stu-id="c680d-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="c680d-144">Quando o usuário inicia um download em segundo plano, partes do arquivo são transferidas para o computador do usuário quando o tempo do processador está disponível.</span><span class="sxs-lookup"><span data-stu-id="c680d-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="c680d-145">É possível pausar e retomar um download em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c680d-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="c680d-146">Se o usuário optar por fechar o Windows Media Player antes de o download em segundo plano ser concluído, a condição de todos os arquivos incompletos será salva e o download poderá continuar em segundo plano, mesmo após a reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="c680d-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="c680d-147">O download em segundo plano pode demorar mais do que o download em tempo real, pois o processo de download ocorre apenas quando o processador não está executando outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="c680d-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="c680d-148">O download em segundo plano só está disponível ao usar o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c680d-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="c680d-149">Sobre a integração de biblioteca</span><span class="sxs-lookup"><span data-stu-id="c680d-149">About Library Integration</span></span>

<span data-ttu-id="c680d-150">O Windows Media Player pode organizar automaticamente o conteúdo da loja online na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c680d-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="c680d-151">Para habilitar isso, você deve especificar um valor para o atributo **WM/ContentDistributor** para cada arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="c680d-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="c680d-152">Quando um arquivo de mídia digital é adicionado à biblioteca, o que acontece automaticamente ao usar o Gerenciador de download, o arquivo é listado automaticamente no nó **música adquirida** ou **vídeos comprados** .</span><span class="sxs-lookup"><span data-stu-id="c680d-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="c680d-153">Por exemplo, se o valor de **WM/ContentDistributor** for "Proseware" e o arquivo de mídia digital contiver música, o conteúdo aparecerá na biblioteca no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="c680d-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="c680d-154">Todas as músicas/Proseware adquiridas</span><span class="sxs-lookup"><span data-stu-id="c680d-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="c680d-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c680d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c680d-156">**Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="c680d-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="c680d-157">**Downloadcollection. startDownload**</span><span class="sxs-lookup"><span data-stu-id="c680d-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




