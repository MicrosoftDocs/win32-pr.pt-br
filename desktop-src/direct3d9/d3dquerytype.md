---
description: Identifica o tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeração D3DQUERYTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7a9c20050e7d0dce5a19664d937c016a475a9a13
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343071"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="21959-103">Enumeração D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="21959-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="21959-104">Identifica o tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="21959-104">Identifies the query type.</span></span> <span data-ttu-id="21959-105">Para obter informações sobre consultas, [consulte Consultas (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="21959-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="21959-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21959-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="21959-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="21959-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="21959-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="21959-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="21959-109">Consulte dicas de driver sobre o layout de dados para cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="21959-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="21959-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="21959-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="21959-111">Consulte o gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="21959-111">Query the resource manager.</span></span> <span data-ttu-id="21959-112">Para essa consulta, os sinalizadores de comportamento do dispositivo devem incluir [D3DCREATE \_ DISABLE \_ DRIVER \_ MANAGEMENT](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="21959-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="21959-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="21959-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-114">Consultar estatísticas de vértice.</span><span class="sxs-lookup"><span data-stu-id="21959-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="21959-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**EVENTO D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="21959-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="21959-116">Consulte todos os eventos assíncronos que foram emitidos de chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="21959-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="21959-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**OCLUSÃO D3DQUERYTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="21959-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="21959-118">Uma consulta de oclusão retorna o número de pixels que passam no teste z.</span><span class="sxs-lookup"><span data-stu-id="21959-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="21959-119">Esses pixels são para primitivos desenhados entre o problema [**de D3DISSUE \_ BEGIN**](d3dissue-begin.md) e [**D3DISSUE \_ END.**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="21959-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="21959-120">Isso permite que um aplicativo verifique o resultado da oclusão em relação a 0.</span><span class="sxs-lookup"><span data-stu-id="21959-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="21959-121">Zero está totalmente ocluído, o que significa que os pixels não são visíveis na posição atual da câmera.</span><span class="sxs-lookup"><span data-stu-id="21959-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="21959-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ TIMESTAMP**</span><span class="sxs-lookup"><span data-stu-id="21959-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="21959-123">Retorna um carimbo de data/hora de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="21959-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="21959-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="21959-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="21959-125">Use essa consulta para notificar um aplicativo se a frequência do contador tiver mudado do \_ carimbo de data/hora D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="21959-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="21959-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="21959-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="21959-127">Esse resultado da consulta será **true** se os valores de \_ consultas de carimbo de data/hora D3DQUERYTYPE não puderem ser contínuos durante a \_ consulta D3DQUERYTYPE TIMESTAMPDISJOINT.</span><span class="sxs-lookup"><span data-stu-id="21959-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="21959-128">Caso contrário, o resultado da consulta será **false**.</span><span class="sxs-lookup"><span data-stu-id="21959-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="21959-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="21959-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-130">Porcentagem de tempo de processamento de dados do pipeline.</span><span class="sxs-lookup"><span data-stu-id="21959-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="21959-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="21959-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-132">Porcentagem de tempo de processamento de dados no driver.</span><span class="sxs-lookup"><span data-stu-id="21959-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="21959-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="21959-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-134">Porcentagem de tempo processando dados do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="21959-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="21959-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="21959-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-136">Porcentagem de tempo processando dados do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="21959-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="21959-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="21959-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="21959-138">Comparações de medição de produtividade para ajudar na compreensão do desempenho de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21959-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="21959-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="21959-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="21959-140">Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="21959-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="21959-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="21959-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="21959-142">Eficiência da alocação de memória contida em uma estrutura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="21959-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="21959-143">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="21959-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="21959-144">D3DQUERYTYPE MEMORYPRESSURE só está disponível no Direct3D9Ex em execução no \_ Windows 7 (ou sistema operacional mais recente).</span><span class="sxs-lookup"><span data-stu-id="21959-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21959-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21959-145">Requirements</span></span>



| <span data-ttu-id="21959-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="21959-146">Requirement</span></span> | <span data-ttu-id="21959-147">Valor</span><span class="sxs-lookup"><span data-stu-id="21959-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21959-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21959-148">Header</span></span><br/> | <dl> <span data-ttu-id="21959-149"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="21959-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21959-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="21959-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21959-151">Enumerações direct3D</span><span class="sxs-lookup"><span data-stu-id="21959-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="21959-152">**IDirect3DDevice9::CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="21959-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
