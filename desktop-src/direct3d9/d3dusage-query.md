---
description: Essas opções identificam os tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038cb64b1ad4f5f7ee2dd78ffc2e2a5ebab90d0e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342981"
---
# <a name="d3dusage_query"></a><span data-ttu-id="d1dab-103">CONSULTA D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="d1dab-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="d1dab-104">Essas opções identificam os tipos de recursos de consulta.</span><span class="sxs-lookup"><span data-stu-id="d1dab-104">These options identify query resource types.</span></span>



| <span data-ttu-id="d1dab-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="d1dab-105">\#define</span></span>                                   | <span data-ttu-id="d1dab-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1dab-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dab-107">FILTRO DE CONSULTA D3DUSAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1dab-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="d1dab-108">Consulte o formato do recurso para ver se ele dá suporte a tipos de filtro de textura diferentes de D3DTEXF \_ POINT (que sempre tem suporte).</span><span class="sxs-lookup"><span data-stu-id="d1dab-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="d1dab-109">D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="d1dab-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="d1dab-110">Consulte o recurso sobre um mapa de aumento herdado.</span><span class="sxs-lookup"><span data-stu-id="d1dab-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d1dab-111">D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING</span><span class="sxs-lookup"><span data-stu-id="d1dab-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="d1dab-112">Consulte o recurso para verificar o suporte para suporte à combinação de sombreador de pixel pós-pixel.</span><span class="sxs-lookup"><span data-stu-id="d1dab-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="d1dab-113">Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) falhar com D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING, não há suporte para operações pós-mesclagem de \_ pixels.</span><span class="sxs-lookup"><span data-stu-id="d1dab-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="d1dab-114">Isso inclui teste alfa, pixel pixel pixel, mesclagem de destino de renderização, habilitação de gravação de cor e dithering.</span><span class="sxs-lookup"><span data-stu-id="d1dab-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="d1dab-115">CONSULTA D3DUSAGE \_ \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="d1dab-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="d1dab-116">Consulte o recurso para verificar se uma textura dá suporte à correção gama durante uma operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="d1dab-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d1dab-117">D3DUSAGE \_ QUERY \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="d1dab-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="d1dab-118">Consulte o recurso para verificar se uma textura dá suporte à correção gama durante uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="d1dab-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d1dab-119">D3DUSAGE \_ QUERY \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="d1dab-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="d1dab-120">Consulte o recurso para verificar o suporte para amostragem de textura do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1dab-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d1dab-121">D3DUSAGE \_ QUERY \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="d1dab-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="d1dab-122">Consulte o recurso para verificar o suporte para disposição de textura e mapeamento de MIP.</span><span class="sxs-lookup"><span data-stu-id="d1dab-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="d1dab-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar o suporte de hardware para esses usos e alguns outros usos listados em [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="d1dab-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d1dab-124">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="d1dab-124">Constant Information</span></span>



| <span data-ttu-id="d1dab-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1dab-125">Requirement</span></span>                         | <span data-ttu-id="d1dab-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d1dab-126">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="d1dab-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1dab-127">Header</span></span>                   | <span data-ttu-id="d1dab-128">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="d1dab-128">d3d9types.h</span></span> |
| <span data-ttu-id="d1dab-129">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="d1dab-129">Minimum operating system</span></span> | <span data-ttu-id="d1dab-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d1dab-130">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="d1dab-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1dab-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1dab-132">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d1dab-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
