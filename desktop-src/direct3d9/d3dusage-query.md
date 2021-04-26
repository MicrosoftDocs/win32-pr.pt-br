---
description: Essas opções identificam os tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994103"
---
# <a name="d3dusage_query"></a><span data-ttu-id="4ec66-103">\_Consulta D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="4ec66-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="4ec66-104">Essas opções identificam os tipos de recursos de consulta.</span><span class="sxs-lookup"><span data-stu-id="4ec66-104">These options identify query resource types.</span></span>



| <span data-ttu-id="4ec66-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="4ec66-105">\#define</span></span>                                   | <span data-ttu-id="4ec66-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ec66-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec66-107">\_Filtro de consulta do D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="4ec66-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="4ec66-108">Consulte o formato de recurso para ver se ele dá suporte a tipos de filtro de textura diferentes do \_ ponto D3DTEXF (que tem sempre suporte).</span><span class="sxs-lookup"><span data-stu-id="4ec66-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="4ec66-109">D3DUSAGE \_ consulta \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="4ec66-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="4ec66-110">Consulte o recurso sobre um mapa de relevo herdado.</span><span class="sxs-lookup"><span data-stu-id="4ec66-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4ec66-111">D3DUSAGE \_ consulta \_ POSTPIXELSHADER \_ Blending</span><span class="sxs-lookup"><span data-stu-id="4ec66-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="4ec66-112">Consulte o recurso para verificar o suporte para o suporte de mesclagem de sombreador de pixel de lançamento.</span><span class="sxs-lookup"><span data-stu-id="4ec66-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="4ec66-113">Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) falhar com a \_ \_ \_ mesclagem POSTPIXELSHADER de consulta D3DUSAGE, não haverá suporte para operações de mesclagem de pixels post.</span><span class="sxs-lookup"><span data-stu-id="4ec66-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="4ec66-114">Isso inclui teste alfa, sombra de pixel, mesclagem de destino de renderização, habilitação de gravação de cor e pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="4ec66-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="4ec66-115">D3DUSAGE \_ consulta \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="4ec66-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="4ec66-116">Consulte o recurso para verificar se uma textura dá suporte à correção de gama durante uma operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="4ec66-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4ec66-117">D3DUSAGE \_ consulta \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="4ec66-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="4ec66-118">Consulte o recurso para verificar se uma textura dá suporte à correção de gama durante uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="4ec66-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4ec66-119">D3DUSAGE \_ consulta \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="4ec66-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="4ec66-120">Consulte o recurso para verificar o suporte para amostragem de textura de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4ec66-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4ec66-121">D3DUSAGE \_ consulta \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="4ec66-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="4ec66-122">Consulte o recurso para verificar o suporte para disposição de textura e mapeamento de MIP.</span><span class="sxs-lookup"><span data-stu-id="4ec66-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="4ec66-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar o suporte de hardware para esses usos e alguns outros usos listados em [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="4ec66-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="4ec66-124">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="4ec66-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="4ec66-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ec66-125">Header</span></span>                   | <span data-ttu-id="4ec66-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="4ec66-126">d3d9types.h</span></span> |
| <span data-ttu-id="4ec66-127">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="4ec66-127">Minimum operating system</span></span> | <span data-ttu-id="4ec66-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4ec66-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="4ec66-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ec66-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec66-130">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="4ec66-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
