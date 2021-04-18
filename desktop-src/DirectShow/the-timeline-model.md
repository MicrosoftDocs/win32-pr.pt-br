---
description: O modelo de linha do tempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: O modelo de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554846"
---
# <a name="the-timeline-model"></a><span data-ttu-id="13ea0-103">O modelo de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="13ea0-103">The Timeline Model</span></span>

<span data-ttu-id="13ea0-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="13ea0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="13ea0-105">Uma *linha do tempo* é um objeto que o [serviço de edição do DirectShow](directshow-editing-services.md) (des) usa para representar um projeto de edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="13ea0-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="13ea0-106">Um projeto de edição é iniciado como uma coleção de clipes de origem, extraídos de arquivos de vídeo, arquivos de som ou arquivos de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="13ea0-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="13ea0-107">Uma sequência linear de clipes formam uma *faixa*. Em serviços de edição do DirectShow (DES), áudio e vídeo são colocados em faixas separadas.</span><span class="sxs-lookup"><span data-stu-id="13ea0-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="13ea0-108">As faixas também podem ser em camadas.</span><span class="sxs-lookup"><span data-stu-id="13ea0-108">Tracks can also be layered.</span></span> <span data-ttu-id="13ea0-109">Várias faixas de áudio são misturadas e podem incluir efeitos de áudio, como fade ou reverberação.</span><span class="sxs-lookup"><span data-stu-id="13ea0-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="13ea0-110">Várias faixas de vídeo são usadas para criar transições.</span><span class="sxs-lookup"><span data-stu-id="13ea0-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="13ea0-111">Por exemplo, você pode criar um apagamento de um clipe para outro.</span><span class="sxs-lookup"><span data-stu-id="13ea0-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="13ea0-112">Outro exemplo é uma chave croma, na qual o plano de fundo de um clipe é inserido e substituído por uma faixa diferente. (O previsão do tempo na frente de uma imagem satelite é um exemplo de croma de chaveamento.)</span><span class="sxs-lookup"><span data-stu-id="13ea0-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="13ea0-113">O DES usa uma estrutura de árvore para representar uma edição:</span><span class="sxs-lookup"><span data-stu-id="13ea0-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="13ea0-114">Os clipes de áudio e vídeo formam os nós folha ou os objetos de *origem* .</span><span class="sxs-lookup"><span data-stu-id="13ea0-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="13ea0-115">Uma coleção de fontes com um tipo de mídia uniforme (áudio ou vídeo) é uma *faixa*.</span><span class="sxs-lookup"><span data-stu-id="13ea0-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="13ea0-116">Uma coleção de faixas é uma *composição*.</span><span class="sxs-lookup"><span data-stu-id="13ea0-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="13ea0-117">Uma composição é renderizada como a composição de todas as faixas que ela contém.</span><span class="sxs-lookup"><span data-stu-id="13ea0-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="13ea0-118">As composições podem conter outras composições, o que permite a organização de faixas complexas.</span><span class="sxs-lookup"><span data-stu-id="13ea0-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="13ea0-119">Uma coleção de alto nível de composições e faixas (todas representando o mesmo tipo de mídia) é um *grupo*.</span><span class="sxs-lookup"><span data-stu-id="13ea0-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="13ea0-120">Um conjunto de um ou mais grupos formam uma *linha do tempo*.</span><span class="sxs-lookup"><span data-stu-id="13ea0-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="13ea0-121">A linha do tempo é o nó raiz na árvore.</span><span class="sxs-lookup"><span data-stu-id="13ea0-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="13ea0-122">Uma linha do tempo deve conter pelo menos um grupo.</span><span class="sxs-lookup"><span data-stu-id="13ea0-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="13ea0-123">Cada grupo representa um único fluxo na produção final.</span><span class="sxs-lookup"><span data-stu-id="13ea0-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="13ea0-124">Um projeto típico inclui um grupo de vídeos e um grupo de áudio.</span><span class="sxs-lookup"><span data-stu-id="13ea0-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="13ea0-125">As composições são opcionais; elas existem para fornecer mais estrutura, se necessário.</span><span class="sxs-lookup"><span data-stu-id="13ea0-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="13ea0-126">A ilustração a seguir mostra as relações filho-pai que compõem uma linha do tempo:</span><span class="sxs-lookup"><span data-stu-id="13ea0-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![estrutura do nó](images/timeline1.png)

<span data-ttu-id="13ea0-128">O seguinte mostra uma linha do tempo como uma sequência temporal:</span><span class="sxs-lookup"><span data-stu-id="13ea0-128">The following shows a timeline as a temporal sequence:</span></span>

![ilustração da linha do tempo](images/timeline2.png)

<span data-ttu-id="13ea0-130">A seta na parte superior representa a direção da linha do tempo, começando do tempo zero.</span><span class="sxs-lookup"><span data-stu-id="13ea0-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="13ea0-131">No grupo de vídeos, Track 1 tem uma prioridade mais alta do que a faixa 0.</span><span class="sxs-lookup"><span data-stu-id="13ea0-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="13ea0-132">Os objetos de origem no Track 1 obscurecem aqueles no Track 0.</span><span class="sxs-lookup"><span data-stu-id="13ea0-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="13ea0-133">Onde Track 1 está vazio, Track 0 "mostra".</span><span class="sxs-lookup"><span data-stu-id="13ea0-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="13ea0-134">Como mencionado anteriormente, as faixas de áudio são simplesmente misturadas juntas.</span><span class="sxs-lookup"><span data-stu-id="13ea0-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13ea0-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13ea0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ea0-136">Introdução com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="13ea0-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="13ea0-137">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="13ea0-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



