---
title: Registro de neblina
description: O registro de saída do sombreador de vértice contém uma cor de neblina por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967038"
---
# <a name="fog-register"></a><span data-ttu-id="10a2b-103">Registro de neblina</span><span class="sxs-lookup"><span data-stu-id="10a2b-103">Fog Register</span></span>

<span data-ttu-id="10a2b-104">O registro de saída do sombreador de vértice contém uma cor de neblina por vértice.</span><span class="sxs-lookup"><span data-stu-id="10a2b-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="10a2b-105">Um registro consiste em propriedades que determinam se o registro se comporta.</span><span class="sxs-lookup"><span data-stu-id="10a2b-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="10a2b-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="10a2b-106">Property</span></span>        | <span data-ttu-id="10a2b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="10a2b-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a2b-108">Name</span><span class="sxs-lookup"><span data-stu-id="10a2b-108">Name</span></span>            | <span data-ttu-id="10a2b-109">oFog</span><span class="sxs-lookup"><span data-stu-id="10a2b-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="10a2b-110">Contagem</span><span class="sxs-lookup"><span data-stu-id="10a2b-110">Count</span></span>           | <span data-ttu-id="10a2b-111">Um vetor, do qual apenas um componente pode ser usado e deve ser especificado pela máscara do componente</span><span class="sxs-lookup"><span data-stu-id="10a2b-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="10a2b-112">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="10a2b-112">I/O permissions</span></span> | <span data-ttu-id="10a2b-113">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="10a2b-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="10a2b-114">O valor de neblina de saída é registrado.</span><span class="sxs-lookup"><span data-stu-id="10a2b-114">The output fog value registers.</span></span> <span data-ttu-id="10a2b-115">O valor é o fator de neblina a ser interpolado e, em seguida, roteado para a tabela de neblina.</span><span class="sxs-lookup"><span data-stu-id="10a2b-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="10a2b-116">Somente o componente x escalar da neblina é usado.</span><span class="sxs-lookup"><span data-stu-id="10a2b-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10a2b-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10a2b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a2b-118">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="10a2b-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




