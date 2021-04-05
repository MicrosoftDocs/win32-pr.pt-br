---
description: Os parâmetros de neblina são controlados por meio de Estados de processamento de dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parâmetros de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825708"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="2ba88-103">Parâmetros de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ba88-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="2ba88-104">Os parâmetros de neblina são controlados por meio de Estados de processamento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ba88-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="2ba88-105">Os tipos de neblina de pixel e Vertex dão suporte a todas as fórmulas de neblina introduzidas em [fórmulas de neblina (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="2ba88-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="2ba88-106">O tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) define constantes que você pode usar para identificar a fórmula de neblina que você deseja que o Microsoft Direct3D use.</span><span class="sxs-lookup"><span data-stu-id="2ba88-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="2ba88-107">O \_ estado de RENDERIZAÇÃO D3DRS FOGTABLEMODE controla o modo de neblina usado pelo Direct3D para a neblina de pixels e o \_ estado de renderização D3DRS FOGVERTEXMODE controla o modo de neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="2ba88-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="2ba88-108">Ao usar a fórmula de neblina linear, você define as distâncias inicial e final por meio dos \_ Estados de RENDERIZAÇÃO D3DRS FOGSTART e D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="2ba88-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="2ba88-109">A maneira como o sistema interpreta esses valores depende do tipo de neblina que seu aplicativo usa – pixel ou neblina de vértice-e, ao usar a neblina de pixel, se a profundidade baseada em z ou w estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="2ba88-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="2ba88-110">A tabela a seguir resume os tipos de neblina e suas unidades de início e de término.</span><span class="sxs-lookup"><span data-stu-id="2ba88-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="2ba88-111">Tipo de neblina</span><span class="sxs-lookup"><span data-stu-id="2ba88-111">Fog type</span></span>  | <span data-ttu-id="2ba88-112">Unidades de início/término da neblina</span><span class="sxs-lookup"><span data-stu-id="2ba88-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="2ba88-113">Pixel (Z)</span><span class="sxs-lookup"><span data-stu-id="2ba88-113">Pixel (Z)</span></span> | <span data-ttu-id="2ba88-114">Espaço \[ de dispositivo 0,0, 1,0\]</span><span class="sxs-lookup"><span data-stu-id="2ba88-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="2ba88-115">Pixel (W)</span><span class="sxs-lookup"><span data-stu-id="2ba88-115">Pixel (W)</span></span> | <span data-ttu-id="2ba88-116">Espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="2ba88-116">Camera space</span></span>             |
| <span data-ttu-id="2ba88-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="2ba88-117">Vertex</span></span>    | <span data-ttu-id="2ba88-118">Espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="2ba88-118">Camera space</span></span>             |



 

<span data-ttu-id="2ba88-119">O \_ estado de RENDERIZAÇÃO D3DRS FOGDENSITY controla a densidade de neblina aplicada quando uma fórmula de neblina exponencial é habilitada.</span><span class="sxs-lookup"><span data-stu-id="2ba88-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="2ba88-120">A densidade de neblina é essencialmente um fator de ponderação, variando de 0,0 a 1,0 (inclusivo), que dimensiona o valor de distância no expoente.</span><span class="sxs-lookup"><span data-stu-id="2ba88-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="2ba88-121">A cor que o sistema usa para mesclagem de neblina é controlada por meio do \_ estado de processamento do dispositivo D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="2ba88-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="2ba88-122">Para obter mais informações, consulte [cor de neblina (Direct3D 9)](fog-color.md) e [mistura de neblina (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="2ba88-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba88-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ba88-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba88-124">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="2ba88-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
