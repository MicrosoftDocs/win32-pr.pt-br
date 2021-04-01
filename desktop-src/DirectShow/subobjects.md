---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829371"
---
# <a name="subobjects"></a><span data-ttu-id="b1209-103">Subobjetos</span><span class="sxs-lookup"><span data-stu-id="b1209-103">Subobjects</span></span>

<span data-ttu-id="b1209-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="b1209-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b1209-105">Fontes, efeitos e transições têm ponteiros internos para outros objetos COM, chamados de *subobjetos*.</span><span class="sxs-lookup"><span data-stu-id="b1209-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="b1209-106">O subobjeto executa o trabalho real do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1209-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="b1209-107">O subobjeto de uma origem é o componente que cria os dados de vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="b1209-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="b1209-108">O subobjeto de um efeito ou transição é o componente que transforma os dados; por exemplo, em um efeito de vídeo, ele cria o efeito visual no fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b1209-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="b1209-109">O tipo de subobjeto depende do tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="b1209-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="b1209-110">Fonte: qualquer filtro de origem ou filtro do analisador do DirectShow que ofereça suporte à busca e produza um formato compatível com o DES.</span><span class="sxs-lookup"><span data-stu-id="b1209-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="b1209-111">Ele pode ser um formato compactado se houver filtros do DirectShow para decodificá-lo.</span><span class="sxs-lookup"><span data-stu-id="b1209-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="b1209-112">Efeito: para vídeo, qualquer objeto de transformação One-D da Microsoft® DirectX® Transform.</span><span class="sxs-lookup"><span data-stu-id="b1209-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="b1209-113">Para áudio, qualquer filtro de efeito de áudio do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b1209-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="b1209-114">Transição: para vídeo, qualquer objeto de transformação DirectX de duas entradas 2-D.</span><span class="sxs-lookup"><span data-stu-id="b1209-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="b1209-115">O áudio não oferece suporte a transições.</span><span class="sxs-lookup"><span data-stu-id="b1209-115">Audio does not support transitions.</span></span>

<span data-ttu-id="b1209-116">Grupos, composições e faixas não têm subobjetos.</span><span class="sxs-lookup"><span data-stu-id="b1209-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="b1209-117">O aplicativo não define diretamente o ponteiro do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="b1209-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="b1209-118">Para efeitos e transições, o aplicativo chama o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar o GUID do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="b1209-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="b1209-119">Para objetos de origem, um aplicativo normalmente chama o [**IAMTimelineSrc:: Setmedianame**](iamtimelinesrc-setmedianame.md) para especificar o nome de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="b1209-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="b1209-120">No entanto, o método **SetSubObjectGUID** também pode ser usado para objetos de origem, para especificar o identificador de classe (CLSID) de um filtro.</span><span class="sxs-lookup"><span data-stu-id="b1209-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="b1209-121">Para obter mais informações, consulte [trabalhando com fontes](working-with-sources.md) e [trabalhando com efeitos e transições](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="b1209-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1209-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1209-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1209-123">Visão geral dos componentes da linha do tempo</span><span class="sxs-lookup"><span data-stu-id="b1209-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



