---
description: Gerenciando projetos de edição de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gerenciando projetos de edição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756608"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="dd90e-103">Gerenciando projetos de edição de vídeo</span><span class="sxs-lookup"><span data-stu-id="dd90e-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="dd90e-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="dd90e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dd90e-105">As dicas a seguir ajudarão você a gerenciar projetos nos [serviços de edição do DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="dd90e-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="dd90e-106">Alterações na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="dd90e-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="dd90e-107">Se você alterar a linha do tempo depois de criar o grafo de filtro, chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) novamente para recriar o front-end.</span><span class="sxs-lookup"><span data-stu-id="dd90e-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="dd90e-108">Normalmente, isso não afeta o restante do grafo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="dd90e-109">Ocasionalmente, no entanto, o mecanismo de renderização precisa excluir o grafo inteiro antes de recompilar o front-end.</span><span class="sxs-lookup"><span data-stu-id="dd90e-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="dd90e-110">(Por exemplo, isso acontece se você adicionar ou remover um grupo.) O método **ConnectFrontEnd** retorna S \_ \_ OUTPUTRESET warn para sinalizar que excluiu o grafo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="dd90e-111">Se isso acontecer, seu aplicativo deverá recriar a seção de renderização do grafo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="dd90e-112">Para remover completamente todos os objetos da linha do tempo, chame o método [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="dd90e-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="dd90e-113">**Limpeza**</span><span class="sxs-lookup"><span data-stu-id="dd90e-113">**Cleanup**</span></span>

-   <span data-ttu-id="dd90e-114">Quando você terminar de usar um mecanismo de renderização, chame o método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="dd90e-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="dd90e-115">Como com qualquer objeto COM, certifique-se de liberar todos os ponteiros de interface quando terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="dd90e-116">O mecanismo de renderização não mantém uma contagem de referência na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="dd90e-117">Não libere a linha do tempo antes de terminar de usá-la e sempre chame **ScrapIt** no mecanismo de processamento primeiro.</span><span class="sxs-lookup"><span data-stu-id="dd90e-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="dd90e-118">Se você liberar todas as referências a uma linha do tempo, não use nenhum dos objetos nessa linha do tempo, mesmo se você estiver mantendo contagens de referência neles.</span><span class="sxs-lookup"><span data-stu-id="dd90e-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="dd90e-119">**Várias instâncias da linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="dd90e-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="dd90e-120">Não mova objetos do cronograma entre as linhas do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="dd90e-121">Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="dd90e-122">A linha do tempo contém um cache interno com informações sobre os objetos que ele cria; mover objetos de linha do tempo pode interromper o cache.</span><span class="sxs-lookup"><span data-stu-id="dd90e-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="dd90e-123">Nunca use a mesma instância de um mecanismo de renderização com mais de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="dd90e-124">O mecanismo de renderização mantém um cache com informações sobre a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="dd90e-125">Várias linhas do tempo interromperão o cache e causarão resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="dd90e-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="dd90e-126">Se você precisar de duas linhas do tempo ativas, faça instâncias separadas de mecanismos de renderização para cada linha do cronograma.</span><span class="sxs-lookup"><span data-stu-id="dd90e-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="dd90e-127">Uma linha do tempo pode usar mais de um mecanismo de renderização, mas não ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="dd90e-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="dd90e-128">Exclua o mecanismo de processamento antigo antes de usar outro mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="dd90e-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="dd90e-129">(Normalmente, você faria isso quando alternar de usando o mecanismo de renderização básico para visualização para o mecanismo de processamento inteligente para gravação de arquivo.)</span><span class="sxs-lookup"><span data-stu-id="dd90e-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="dd90e-130">**Persistência**</span><span class="sxs-lookup"><span data-stu-id="dd90e-130">**Persistence**</span></span>

-   <span data-ttu-id="dd90e-131">O grafo de filtro não é persistente quando você salva o projeto em um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="dd90e-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="dd90e-132">Portanto, você perde todas as informações relacionadas à recompactação inteligente, ao formato de compactação ou aos parâmetros de compactação.</span><span class="sxs-lookup"><span data-stu-id="dd90e-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="dd90e-133">Cabe ao aplicativo restaurar esses parâmetros depois de carregar um projeto.</span><span class="sxs-lookup"><span data-stu-id="dd90e-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd90e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd90e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd90e-135">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="dd90e-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



