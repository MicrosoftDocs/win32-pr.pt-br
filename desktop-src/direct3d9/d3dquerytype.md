---
description: Identifica o tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeração D3DQUERYTYPE (D3D9Types. h)
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
ms.openlocfilehash: 0778e879a6147c185964808ee4b4c302bd211ef3
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489690"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="61534-103">Enumeração D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="61534-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="61534-104">Identifica o tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="61534-104">Identifies the query type.</span></span> <span data-ttu-id="61534-105">Para obter informações sobre consultas, consulte [consultas (Direct3D 9)](queries.md)</span><span class="sxs-lookup"><span data-stu-id="61534-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="61534-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61534-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
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



## <a name="constants"></a><span data-ttu-id="61534-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="61534-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61534-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="61534-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="61534-109">Consulte Dicas de driver sobre o layout de dados para o cache de vértice.</span><span class="sxs-lookup"><span data-stu-id="61534-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="61534-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**\_RESOURCEMANAGER D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="61534-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="61534-111">Consulte o Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="61534-111">Query the resource manager.</span></span> <span data-ttu-id="61534-112">Para essa consulta, os sinalizadores de comportamento do dispositivo devem incluir [D3DCREATE \_ desabilitar o \_ \_ Gerenciamento de driver](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="61534-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="61534-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="61534-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-114">Estatísticas de vértice da consulta.</span><span class="sxs-lookup"><span data-stu-id="61534-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="61534-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Evento D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="61534-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="61534-116">Consultar qualquer e todos os eventos assíncronos que foram emitidos de chamadas de API.</span><span class="sxs-lookup"><span data-stu-id="61534-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="61534-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ oclusão**</span><span class="sxs-lookup"><span data-stu-id="61534-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="61534-118">Uma consulta oclusão retorna o número de pixels que passam testes em z.</span><span class="sxs-lookup"><span data-stu-id="61534-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="61534-119">Esses pixels são para primitivos desenhados entre o problema de [**D3DISSUE \_ begin**](d3dissue-begin.md) e [**D3DISSUE \_ end**](d3dissue-end.md).</span><span class="sxs-lookup"><span data-stu-id="61534-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="61534-120">Isso permite que um aplicativo Verifique o resultado do oclusão em relação a 0.</span><span class="sxs-lookup"><span data-stu-id="61534-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="61534-121">Zero é totalmente obstruído, o que significa que os pixels não são visíveis na posição atual da câmera.</span><span class="sxs-lookup"><span data-stu-id="61534-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="61534-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Carimbo de data/hora D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="61534-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="61534-123">Retorna um carimbo de data/hora de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="61534-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="61534-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="61534-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="61534-125">Use essa consulta para notificar um aplicativo se a frequência do contador tiver mudado do \_ carimbo de data/hora D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="61534-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="61534-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="61534-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="61534-127">Esse resultado da consulta será **true** se os valores de \_ consultas de carimbo de data/hora D3DQUERYTYPE não puderem ser contínuos durante a \_ consulta D3DQUERYTYPE TIMESTAMPDISJOINT.</span><span class="sxs-lookup"><span data-stu-id="61534-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="61534-128">Caso contrário, o resultado da consulta será **false**.</span><span class="sxs-lookup"><span data-stu-id="61534-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="61534-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="61534-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-130">Porcentagem de tempo de processamento de dados do pipeline.</span><span class="sxs-lookup"><span data-stu-id="61534-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="61534-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="61534-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-132">Porcentagem de tempo de processamento de dados no driver.</span><span class="sxs-lookup"><span data-stu-id="61534-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="61534-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="61534-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-134">Porcentagem de tempo processando dados do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="61534-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="61534-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="61534-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-136">Porcentagem de tempo processando dados do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="61534-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="61534-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="61534-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="61534-138">Comparações de medição de produtividade para ajudar na compreensão do desempenho de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61534-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="61534-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="61534-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="61534-140">Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="61534-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="61534-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="61534-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="61534-142">Eficiência da alocação de memória contida em uma estrutura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="61534-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="61534-143">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="61534-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="61534-144">o D3DQUERYTYPE \_ MEMORYPRESSURE só está disponível no Direct3D9Ex em execução no Windows 7 (ou mais no sistema operacional atual).</span><span class="sxs-lookup"><span data-stu-id="61534-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61534-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61534-145">Requirements</span></span>



| <span data-ttu-id="61534-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="61534-146">Requirement</span></span> | <span data-ttu-id="61534-147">Valor</span><span class="sxs-lookup"><span data-stu-id="61534-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61534-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61534-148">Header</span></span><br/> | <dl> <span data-ttu-id="61534-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="61534-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61534-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="61534-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61534-151">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="61534-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="61534-152">**IDirect3DDevice9:: CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="61534-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
