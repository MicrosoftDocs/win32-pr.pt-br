---
title: Sobre o tipo 1 lojas online
description: Sobre o tipo 1 lojas online
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Lojas online do Windows Media Player, tipo 1 lojas online
- lojas online, tipo 1 lojas online
- Digite 1 lojas online, sobre
- Windows Media Player, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813393"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="e3203-107">Sobre o tipo 1 lojas online</span><span class="sxs-lookup"><span data-stu-id="e3203-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="e3203-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="e3203-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e3203-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="e3203-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e3203-110">O Microsoft Windows Media Player 11 dá suporte a dois tipos de lojas online: tipo 1 e tipo 2.</span><span class="sxs-lookup"><span data-stu-id="e3203-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="e3203-111">Os armazenamentos do tipo 1 são mais profundamente integrados ao Windows Media Player do que os repositórios do tipo 2.</span><span class="sxs-lookup"><span data-stu-id="e3203-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="e3203-112">Uma loja online tipo 1 fornece um catálogo de música baixável para que o Windows Media Player possa disponibilizar o conteúdo da loja para o usuário como se o conteúdo estivesse na biblioteca de mídia local do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3203-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="e3203-113">Um repositório online tipo 1 deve fornecer um plug-in que implementa a interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="e3203-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="e3203-114">À medida que o usuário navega na interface do usuário do Windows Media Player, o Player chama o plug-in para que a loja online possa aprimorar a experiência do usuário fornecendo páginas da Web que são exibidas no Player.</span><span class="sxs-lookup"><span data-stu-id="e3203-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="e3203-115">Os recursos de repositórios online do tipo 1 que os distinguem dos repositórios do tipo 2 incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3203-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="e3203-116">**Facilidade de uso.**</span><span class="sxs-lookup"><span data-stu-id="e3203-116">**Ease of use.**</span></span> <span data-ttu-id="e3203-117">Os usuários podem procurar música do catálogo de loja online usando a mesma interface do usuário familiar do Windows Media Player que eles usam atualmente para gerenciar sua biblioteca pessoal.</span><span class="sxs-lookup"><span data-stu-id="e3203-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="e3203-118">Os usuários podem exibir apenas um único catálogo de loja online no recurso de procura em qualquer momento específico.</span><span class="sxs-lookup"><span data-stu-id="e3203-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="e3203-119">**Necessidade.**</span><span class="sxs-lookup"><span data-stu-id="e3203-119">**Convenience.**</span></span> <span data-ttu-id="e3203-120">Os usuários podem obter amostras ou comprar música sem alternar do recurso procurar para outra parte da interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e3203-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="e3203-121">**Recursos avançados.**</span><span class="sxs-lookup"><span data-stu-id="e3203-121">**Rich features.**</span></span> <span data-ttu-id="e3203-122">Como o catálogo de loja online é armazenado de maneira semelhante à biblioteca do usuário, muitos dos recursos da biblioteca do Windows Media Player podem ser aplicados ao catálogo.</span><span class="sxs-lookup"><span data-stu-id="e3203-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="e3203-123">Por exemplo, os usuários podem usar a roda de palavras do recurso procurar para filtrar o catálogo de loja online.</span><span class="sxs-lookup"><span data-stu-id="e3203-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="e3203-124">Para um provedor de loja online, as vantagens de fornecer um repositório tipo 1 em vez de um repositório tipo 2 incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3203-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="e3203-125">Um nó personalizado altamente visível na árvore de biblioteca do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e3203-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="e3203-126">Um sistema projetado para compras de música.</span><span class="sxs-lookup"><span data-stu-id="e3203-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="e3203-127">Conexões aprimoradas para processos do Player.</span><span class="sxs-lookup"><span data-stu-id="e3203-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="e3203-128">Um Gerenciador de download melhor e mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="e3203-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="e3203-129">A capacidade de navegar entre vários recursos no Player (incluindo a abertura de nós específicos da árvore de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="e3203-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="e3203-130">Notificações sobre a expiração da licença para o conteúdo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3203-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="e3203-131">Notificações para trabalhar com players de música portáteis conectados.</span><span class="sxs-lookup"><span data-stu-id="e3203-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="e3203-132">As seções a seguir fornecem informações gerais sobre as lojas online do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="e3203-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="e3203-133">Seção</span><span class="sxs-lookup"><span data-stu-id="e3203-133">Section</span></span>                                                                                              | <span data-ttu-id="e3203-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3203-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3203-135">Catálogo de música</span><span class="sxs-lookup"><span data-stu-id="e3203-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="e3203-136">Descreve o catálogo de música fornecido pela loja online.</span><span class="sxs-lookup"><span data-stu-id="e3203-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="e3203-137">Descreve o compilador de catálogo fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e3203-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="e3203-138">Contêineres de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e3203-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="e3203-139">Descreve a[IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)(interface de contêiner de conteúdo), que é usada para representar uma coleção de itens de mídia a serem comprados ou baixados.</span><span class="sxs-lookup"><span data-stu-id="e3203-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="e3203-140">Integração de biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3203-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="e3203-141">Descreve como o catálogo de música do repositório online é integrado à exibição de biblioteca do Player.</span><span class="sxs-lookup"><span data-stu-id="e3203-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="e3203-142">Páginas de descoberta</span><span class="sxs-lookup"><span data-stu-id="e3203-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="e3203-143">Descreve a interação entre o Windows Media Player e as páginas da Web fornecidas pela loja online.</span><span class="sxs-lookup"><span data-stu-id="e3203-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="e3203-144">Menus de contexto</span><span class="sxs-lookup"><span data-stu-id="e3203-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="e3203-145">Descreve como o armazenamento online pode fornecer menus de contexto à medida que o usuário navega pela interface do usuário do jogador.</span><span class="sxs-lookup"><span data-stu-id="e3203-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="e3203-146">Fluxos de áudio</span><span class="sxs-lookup"><span data-stu-id="e3203-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="e3203-147">Descreve como a loja online fornece ao Windows Media Player a URL para o conteúdo de streaming de áudio.</span><span class="sxs-lookup"><span data-stu-id="e3203-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="e3203-148">Documento do serviceInfo para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="e3203-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="e3203-149">Descreve o documento XML do serviceInfo fornecido por um repositório online tipo 1.</span><span class="sxs-lookup"><span data-stu-id="e3203-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="e3203-150">Tipo 1 plug-in de loja online</span><span class="sxs-lookup"><span data-stu-id="e3203-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="e3203-151">Descreve o plug-in que um repositório online tipo 1 deve fornecer.</span><span class="sxs-lookup"><span data-stu-id="e3203-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="e3203-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3203-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3203-153">**Tipos 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="e3203-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




