---
title: Referência do HLSL do Direct3D 12 raytracing
description: Esta seção fornece informações sobre as construções HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7522d26eef8d3c9865a456a94fbd7eafdf99604f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782781"
---
# <a name="raytracing-hlsl-reference"></a><span data-ttu-id="aeaed-103">Referência do raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="aeaed-103">Raytracing HLSL reference</span></span>

<span data-ttu-id="aeaed-104">Esta seção fornece informações sobre as construções HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-104">This section provides information on the HLSL constructs that support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aeaed-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aeaed-105">In this section</span></span>

| <span data-ttu-id="aeaed-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="aeaed-106">Topic</span></span> | <span data-ttu-id="aeaed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aeaed-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="aeaed-108">Enumerações HLSL do Direct3D 12 raytracing</span><span class="sxs-lookup"><span data-stu-id="aeaed-108">Direct3D 12 raytracing HLSL enumerations</span></span>](direct3d-12-raytracing-hlsl-enumerations.md) | <span data-ttu-id="aeaed-109">Descreve as enumerações HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-109">Describes the HLSL enumerations that support the Direct3D 12 raytracing pipeline.</span></span>  |
| [<span data-ttu-id="aeaed-110">Raytracing HLSL intrínsecos do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="aeaed-110">Direct3D 12 raytracing HLSL intrinsics</span></span>](direct3d-12-raytracing-hlsl-intrinsics.md) | <span data-ttu-id="aeaed-111">Descreve o HLSL instrinsics que dá suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-111">Describes the HLSL instrinsics that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="aeaed-112">Tipos de recursos HLSL do Direct3D 12 raytracing</span><span class="sxs-lookup"><span data-stu-id="aeaed-112">Direct3D 12 raytracing HLSL resource types</span></span>](direct3d-12-raytracing-hlsl-resource-types.md) | <span data-ttu-id="aeaed-113">Descreve os tipos de recursos HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-113">Describes the HLSL resource types that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="aeaed-114">Sombreadores do HLSL do Direct3D 12 raytracing</span><span class="sxs-lookup"><span data-stu-id="aeaed-114">Direct3D 12 raytracing HLSL shaders</span></span>](direct3d-12-raytracing-hlsl-shaders.md) | <span data-ttu-id="aeaed-115">Descreve os sombreadores HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-115">Describes the HLSL shaders that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="aeaed-116">Estruturas HLSL do Direct3D 12 raytracing</span><span class="sxs-lookup"><span data-stu-id="aeaed-116">Direct3D 12 raytracing HLSL structures</span></span>](direct3d-12-raytracing-hlsl-structures.md) | <span data-ttu-id="aeaed-117">Descreve as estruturas HLSL que dão suporte ao pipeline do Direct3D 12 raytracing.</span><span class="sxs-lookup"><span data-stu-id="aeaed-117">Describes the HLSL structures that support the Direct3D 12 raytracing pipeline.</span></span> |

<span data-ttu-id="aeaed-118">Além disso, consulte os [objetos de estado](../direct3dhlsl/dx-graphics-hlsl-state-object.md) do tópico para obter informações sobre a sintaxe usada para definir objetos de estado do Direct3D 12 RAYTRACING no HLSL.</span><span class="sxs-lookup"><span data-stu-id="aeaed-118">Additionally, see the topic [State objects](../direct3dhlsl/dx-graphics-hlsl-state-object.md) for information about the syntax used for defining Direct3D 12 raytracing state objects in HLSL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeaed-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aeaed-119">Related topics</span></span>

* [<span data-ttu-id="aeaed-120">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="aeaed-120">Direct3D 12 reference</span></span>](direct3d-12-reference.md)