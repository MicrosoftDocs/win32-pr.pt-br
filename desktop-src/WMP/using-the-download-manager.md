---
title: Usando o Gerenciador de download
description: Usando o Gerenciador de download
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364451"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="33003-109">Usando o Gerenciador de download</span><span class="sxs-lookup"><span data-stu-id="33003-109">Using the Download Manager</span></span>

<span data-ttu-id="33003-110">O SDK do Windows Media Player inclui uma página da Web de exemplo que demonstra o uso do Gerenciador de download para baixar arquivos para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="33003-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="33003-111">Você pode localizar o exemplo na pasta chamada página da Web em que você instalou o SDK.</span><span class="sxs-lookup"><span data-stu-id="33003-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="33003-112">O nome do arquivo é Sample. ASP.</span><span class="sxs-lookup"><span data-stu-id="33003-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="33003-113">O exemplo fornece a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="33003-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="33003-114">Cria o objeto **DownloadManager** .</span><span class="sxs-lookup"><span data-stu-id="33003-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="33003-115">Cria um objeto **downloadcollection** .</span><span class="sxs-lookup"><span data-stu-id="33003-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="33003-116">Inicia o download de cinco arquivos quando o usuário clica em **baixar**.</span><span class="sxs-lookup"><span data-stu-id="33003-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="33003-117">Os caminhos de arquivo padrão são fornecidos no exemplo.</span><span class="sxs-lookup"><span data-stu-id="33003-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="33003-118">Você deve substituir esses caminhos padrão por locais de arquivos em seu próprio servidor.</span><span class="sxs-lookup"><span data-stu-id="33003-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="33003-119">Você pode alterar os caminhos alterando os valores atribuídos à matriz global chamada g \_ sFiles.</span><span class="sxs-lookup"><span data-stu-id="33003-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="33003-120">Mostra informações de status de um download quando o usuário o seleciona.</span><span class="sxs-lookup"><span data-stu-id="33003-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="33003-121">Fornece controles para pausar, retomar, cancelar e remover um item de download.</span><span class="sxs-lookup"><span data-stu-id="33003-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="33003-122">Mantém informações sobre o download de coleções entre sessões usando cookies.</span><span class="sxs-lookup"><span data-stu-id="33003-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="33003-123">Isso é importante porque o usuário pode fechar o Player a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="33003-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="33003-124">Além disso, se o usuário alternar os painéis de tarefas no Player, a sessão da loja online será encerrada.</span><span class="sxs-lookup"><span data-stu-id="33003-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="33003-125">Usa o download em tempo real por padrão.</span><span class="sxs-lookup"><span data-stu-id="33003-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="33003-126">Você pode alterar o comportamento para download em segundo plano alterando o valor da variável chamada g \_ sDLType.</span><span class="sxs-lookup"><span data-stu-id="33003-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="33003-127">O download em segundo plano está disponível para uso com o sistema operacional Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33003-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="33003-128">Sincroniza a cor do plano de fundo com a cor do jogador.</span><span class="sxs-lookup"><span data-stu-id="33003-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="33003-129">Você pode usar esse recurso para fazer com que sua loja online altere a aparência quando o usuário optar por alterar a cor do Player.</span><span class="sxs-lookup"><span data-stu-id="33003-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="33003-130">As seções a seguir fornecem mais informações:</span><span class="sxs-lookup"><span data-stu-id="33003-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="33003-131">Inicializando a página</span><span class="sxs-lookup"><span data-stu-id="33003-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="33003-132">Iniciando os downloads</span><span class="sxs-lookup"><span data-stu-id="33003-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="33003-133">Recuperando informações de status</span><span class="sxs-lookup"><span data-stu-id="33003-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="33003-134">Mantendo informações da sessão</span><span class="sxs-lookup"><span data-stu-id="33003-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="33003-135">Depurando a página</span><span class="sxs-lookup"><span data-stu-id="33003-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="33003-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33003-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33003-137">**Guia de programação para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="33003-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




