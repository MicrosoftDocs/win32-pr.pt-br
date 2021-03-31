---
title: Streaming de mídia avançada
description: Streaming de mídia avançada
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, apresentações baseadas na Web
- Modelo de objeto do Windows Media Player, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Mobile, apresentações baseadas na Web
- Controle ActiveX do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX móvel do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX, apresentações baseadas na Web
- Windows Media Player, streaming de mídia avançada
- Modelo de objeto do Windows Media Player, streaming de mídia avançada
- modelo de objeto, streaming de mídia avançada
- Windows Media Player Mobile, streaming de mídia avançada
- Controle ActiveX do Windows Media Player, streaming de mídia avançada
- Controle ActiveX móvel do Windows Media Player, streaming de mídia avançada
- Controle ActiveX, streaming de mídia avançada
- Apresentações baseadas na Web, streaming de mídia avançada
- Criando apresentações baseadas na Web, streaming de mídia avançado
- streaming de mídia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636640"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="85c1c-120">Streaming de mídia avançada</span><span class="sxs-lookup"><span data-stu-id="85c1c-120">Rich Media Streaming</span></span>

<span data-ttu-id="85c1c-121">Páginas da Web complexas contêm muitos componentes diferentes que normalmente são transferidos separadamente.</span><span class="sxs-lookup"><span data-stu-id="85c1c-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="85c1c-122">Em uma conexão lenta, essas páginas exibem uma peça por vez e podem levar vários minutos para serem exibidas completamente.</span><span class="sxs-lookup"><span data-stu-id="85c1c-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="85c1c-123">Isso pode impedi-lo de sincronizar efetivamente páginas da Web com sua mídia digital.</span><span class="sxs-lookup"><span data-stu-id="85c1c-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="85c1c-124">A solução para esse problema é streaming de mídia avançada, o que significa adicionar suas páginas da Web ao seu fluxo de mídia digital para que elas sejam entregues ao mesmo tempo que os dados de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="85c1c-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="85c1c-125">O streaming de mídia avançada usa um layout simples de conjunto de quadros e se comporta exatamente como a inversão normal de URL.</span><span class="sxs-lookup"><span data-stu-id="85c1c-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="85c1c-126">Assim como na inversão de URL, os comandos de script de URL inseridos em fluxos de mídia digital são usados para exibir o conteúdo no quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="85c1c-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="85c1c-127">Em vez de apontar para páginas na Web, no entanto, os comandos de script de URL são usados pelo Windows Media Player 9 Series ou posterior para acessar arquivos no cache do Internet Explorer em que o conteúdo HTML transmitido é colocado conforme ele é recebido.</span><span class="sxs-lookup"><span data-stu-id="85c1c-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="85c1c-128">Assim como acontece com a inversão de URL normal, você pode escrever manipuladores de eventos que respondam a esses comandos de script de URL ou pode deixar o controle do Windows Media Player controlar tudo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="85c1c-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="85c1c-129">Qualquer conteúdo HTML entregue por meio de streaming de mídia avançada é reproduzido na zona de segurança da Internet e está sujeito às configurações de segurança do navegador do usuário.</span><span class="sxs-lookup"><span data-stu-id="85c1c-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="85c1c-130">Para obter mais informações sobre como criar apresentações de mídia avançadas, consulte o SDK do Windows Media Format 9 Series ou posterior e o SDK do Windows Media Encoder 9 Series.</span><span class="sxs-lookup"><span data-stu-id="85c1c-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85c1c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85c1c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85c1c-132">**Criando Web-Based apresentações**</span><span class="sxs-lookup"><span data-stu-id="85c1c-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="85c1c-133">**Usando o script para controlar a inversão de URL**</span><span class="sxs-lookup"><span data-stu-id="85c1c-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




