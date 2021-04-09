---
description: Texturas são uma ferramenta poderosa para criar realismo em imagens 3D geradas por computador. O Direct3D dá suporte a um amplo conjunto de recursos de texturização, fornecendo aos desenvolvedores acesso fácil a técnicas avançadas de texturização.
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: Texturas do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087249"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="d9eb7-104">Texturas do Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="d9eb7-105">Texturas são uma ferramenta poderosa para criar realismo em imagens 3D geradas por computador.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="d9eb7-106">O Direct3D dá suporte a um amplo conjunto de recursos de texturização, fornecendo aos desenvolvedores acesso fácil a técnicas avançadas de texturização.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="d9eb7-107">Esta seção o ajudará a começar a usar texturas.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="d9eb7-108">Conceitos básicos de texturing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="d9eb7-109">Coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="d9eb7-110">Filtragem de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="d9eb7-111">Recursos de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="d9eb7-112">Disposição de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="d9eb7-113">Mesclagem de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="d9eb7-114">Esses tópicos entrarão em mais detalhes sobre a funcionalidade adicional do texturing.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="d9eb7-115">Geração automática de mipmaps (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="d9eb7-116">Gerenciamento automático de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="d9eb7-117">Recursos de textura compactados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="d9eb7-118">Considerações de hardware para texturing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="d9eb7-119">Recursos de textura de volume (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9eb7-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="d9eb7-120">Para melhorar o desempenho, é recomendável usar texturas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="d9eb7-121">Uma textura dinâmica pode ser bloqueada, gravada e desbloqueada em cada quadro.</span><span class="sxs-lookup"><span data-stu-id="d9eb7-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="d9eb7-122">Consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="d9eb7-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9eb7-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9eb7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9eb7-124">Introdução</span><span class="sxs-lookup"><span data-stu-id="d9eb7-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



