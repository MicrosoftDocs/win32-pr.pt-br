---
description: As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Enumerações de recursos (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010294"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="43b8a-103">Enumerações de recursos (gráficos do Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43b8a-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="43b8a-104">As enumerações a seguir são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="43b8a-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="43b8a-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="43b8a-105">Enumeration</span></span>                                                     | <span data-ttu-id="43b8a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="43b8a-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43b8a-107">**\_Sinalizador de associação de d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="43b8a-108">Identifica como um recurso será usado pelo pipeline e determina a quais estágios de pipeline um recurso pode ser associado.</span><span class="sxs-lookup"><span data-stu-id="43b8a-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="43b8a-109">**\_Sinalizador de \_ acesso de CPU d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="43b8a-110">Especifica os tipos de acesso de CPU permitidos para um recurso.</span><span class="sxs-lookup"><span data-stu-id="43b8a-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="43b8a-111">**\_Dimensão DSV \_ d3d10**</span><span class="sxs-lookup"><span data-stu-id="43b8a-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="43b8a-112">Especifica como acessar um recurso que é usado em uma exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="43b8a-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="43b8a-113">**\_Mapa d3d10**</span><span class="sxs-lookup"><span data-stu-id="43b8a-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="43b8a-114">Identifica um recurso a ser mapeado para leitura e gravação pela CPU.</span><span class="sxs-lookup"><span data-stu-id="43b8a-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="43b8a-115">**\_Sinalizador de mapa de d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="43b8a-116">Especifica como a CPU deve responder a qualquer método de mapa quando a GPU ainda não tiver sido concluída com o recurso.</span><span class="sxs-lookup"><span data-stu-id="43b8a-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="43b8a-117">**\_Dimensão de recurso d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="43b8a-118">Identifica o tipo de recurso que está em uso.</span><span class="sxs-lookup"><span data-stu-id="43b8a-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="43b8a-119">**\_ \_ Sinalizador diverso de recurso d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="43b8a-120">Identifica opções de criação de recursos menos comuns.</span><span class="sxs-lookup"><span data-stu-id="43b8a-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="43b8a-121">**\_Dimensão d3d10 RTV \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="43b8a-122">Especifica como acessar um recurso usado em uma exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="43b8a-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="43b8a-123">**Uso de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="43b8a-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="43b8a-124">Identifica como um recurso deve ser lido e gravado pela CPU e/ou pela GPU.</span><span class="sxs-lookup"><span data-stu-id="43b8a-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="43b8a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43b8a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43b8a-126">Referência de recurso</span><span class="sxs-lookup"><span data-stu-id="43b8a-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



