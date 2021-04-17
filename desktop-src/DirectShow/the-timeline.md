---
description: A linha do tempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: A linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760870"
---
# <a name="the-timeline"></a><span data-ttu-id="74cb0-103">A linha do tempo</span><span class="sxs-lookup"><span data-stu-id="74cb0-103">The Timeline</span></span>

<span data-ttu-id="74cb0-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="74cb0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="74cb0-105">A linha do tempo expõe a interface [**IAMTimeline**](iamtimeline.md) .</span><span class="sxs-lookup"><span data-stu-id="74cb0-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="74cb0-106">Esta interface contém métodos para definir propriedades na linha do tempo; para adicionar grupos à linha do tempo; e para criar objetos de linha do tempo, como grupos, faixas e fontes.</span><span class="sxs-lookup"><span data-stu-id="74cb0-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="74cb0-107">Para criar uma nova linha do tempo, chame a função **CoCreateInstance** padrão da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="74cb0-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="74cb0-108">A nova linha do tempo está vazia.</span><span class="sxs-lookup"><span data-stu-id="74cb0-108">The new timeline is empty.</span></span> <span data-ttu-id="74cb0-109">Neste ponto, você pode carregar um arquivo de projeto existente (consulte [carregando e visualizando um projeto](loading-and-previewing-a-project.md)), ou criar a linha do tempo criando e inserindo novos objetos (consulte [construindo uma linha do tempo](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="74cb0-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74cb0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74cb0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74cb0-111">Visão geral dos componentes da linha do tempo</span><span class="sxs-lookup"><span data-stu-id="74cb0-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



