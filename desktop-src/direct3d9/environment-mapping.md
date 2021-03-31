---
description: O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o Ray tracing.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapeamento de ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645762"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="3d7c3-103">Mapeamento de ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3d7c3-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="3d7c3-104">O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o Ray tracing.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="3d7c3-105">Na prática, o mapeamento de ambiente aplica um mapa de textura especial que contém uma imagem da cena em torno de um objeto ao próprio objeto.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="3d7c3-106">O resultado aproxima a aparência de uma superfície reflexiva, perto o suficiente para enganar o olho, sem incorrer em nenhum cálculo complexo envolvido no rastreamento de Ray.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="3d7c3-107">A ilustração a seguir demonstra um tipo de mapeamento de ambiente chamado de mapeamento de ambiente esférico.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="3d7c3-108">Para obter detalhes, consulte [mapeamento de ambiente esférico](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="3d7c3-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![ilustração de um bule com uma textura aplicada que reflete os arredores](images/spheremapped-teapot.png)

<span data-ttu-id="3d7c3-110">O bule nessa imagem parece refletir seu ambiente; na verdade, essa é uma textura que está sendo aplicada ao objeto.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="3d7c3-111">Como o mapeamento de ambiente usa uma textura, combinada com coordenadas de textura especialmente computadas, ela pode ser executada em tempo real.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="3d7c3-112">Esta seção fornece informações sobre como executar dois tipos comuns de mapeamento de ambiente com o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="3d7c3-113">Há muitos tipos de mapeamento de ambiente em uso em todo o setor de gráficos, mas os seguintes tópicos visam os dois formulários mais comuns: mapeamento de ambiente cúbico e mapeamento de ambiente esférico.</span><span class="sxs-lookup"><span data-stu-id="3d7c3-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="3d7c3-114">Mapeamento de ambiente cúbico</span><span class="sxs-lookup"><span data-stu-id="3d7c3-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="3d7c3-115">Mapeamento de ambiente esférico</span><span class="sxs-lookup"><span data-stu-id="3d7c3-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="3d7c3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d7c3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d7c3-117">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="3d7c3-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



