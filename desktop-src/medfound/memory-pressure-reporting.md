---
description: O relatório de demanda de memória permite que um aplicativo do Direct3D determine quando seu conjunto de trabalho de memória de vídeo cresceu muito grande.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Relatório de pressão de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812804"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="dcc49-103">Relatório de pressão de memória</span><span class="sxs-lookup"><span data-stu-id="dcc49-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="dcc49-104">O relatório de demanda de memória permite que um aplicativo do Direct3D determine quando seu conjunto de trabalho de memória de vídeo cresceu muito grande.</span><span class="sxs-lookup"><span data-stu-id="dcc49-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="dcc49-105">A *pressão de memória* é a demanda colocada no subsistema de memória por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcc49-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="dcc49-106">Embora qualquer aplicativo Direct3D possa usar o relatório de pressão de memória, esse recurso é especialmente útil para aplicativos que renderizam vídeo usando o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dcc49-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="dcc49-107">A reprodução de vídeo normalmente se beneficia de grandes quantidades de buffer, para que os quadros possam ser decodificados antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="dcc49-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="dcc49-108">Embora o armazenamento em buffer geralmente resulte em uma reprodução mais suave, isso pode prejudicar o desempenho se o conjunto de trabalho ficar muito grande, devido aos seguintes fatores:</span><span class="sxs-lookup"><span data-stu-id="dcc49-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="dcc49-109">A memória pode ser removida do cache.</span><span class="sxs-lookup"><span data-stu-id="dcc49-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="dcc49-110">Na pior das hipóteses, isso pode ocorrer em cada quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dcc49-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="dcc49-111">As alocações de memória podem ser colocadas em segmentos de memória não ideais.</span><span class="sxs-lookup"><span data-stu-id="dcc49-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="dcc49-112">A partir do Windows 7, o Direct3D pode relatar algumas estatísticas sobre a pressão da memória de vídeo:</span><span class="sxs-lookup"><span data-stu-id="dcc49-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="dcc49-113">O número de bytes removidos pelo processo durante um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="dcc49-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="dcc49-114">A quantidade de memória colocada em segmentos de memória não ideais.</span><span class="sxs-lookup"><span data-stu-id="dcc49-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="dcc49-115">Uma indicação aproximada da eficiência geral das alocações de memória colocadas na memória não ideal.</span><span class="sxs-lookup"><span data-stu-id="dcc49-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="dcc49-116">Essas informações podem ajudar um aplicativo a manter um conjunto de trabalho razoável.</span><span class="sxs-lookup"><span data-stu-id="dcc49-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="dcc49-117">Usando o relatório de pressão de memória</span><span class="sxs-lookup"><span data-stu-id="dcc49-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="dcc49-118">O relatório de demanda de memória usa a interface **IDirect3DQuery9** existente para consultar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dcc49-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="dcc49-119">Um novo tipo de consulta foi adicionado à enumeração **D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="dcc49-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="dcc49-120">Para usar essa consulta, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="dcc49-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="dcc49-121">Chame **IDirect3DDevice9Ex:: CreateQuery** com o sinalizador **D3DQUERYTYPE \_ MEMORYPRESSURE** .</span><span class="sxs-lookup"><span data-stu-id="dcc49-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="dcc49-122">Esse método retorna um ponteiro para a interface **IDirect3DQuery9** .</span><span class="sxs-lookup"><span data-stu-id="dcc49-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="dcc49-123">Chame **IDirect3DQuery9:: Issue** com o sinalizador de **\_ início D3DISSUE** para iniciar o intervalo de medição.</span><span class="sxs-lookup"><span data-stu-id="dcc49-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="dcc49-124">Chame **IDirect3DQuery9:: Issue** com o sinalizador de **\_ finalização de D3DISSUE** .</span><span class="sxs-lookup"><span data-stu-id="dcc49-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="dcc49-125">Chame **IDirect3DQuery9:: GetData** para obter o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="dcc49-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="dcc49-126">A consulta retorna uma estrutura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc49-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="dcc49-127">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="dcc49-127">Example Code</span></span>

<span data-ttu-id="dcc49-128">O exemplo a seguir mostra duas funções que medem a pressão de memória.</span><span class="sxs-lookup"><span data-stu-id="dcc49-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="dcc49-129">O primeiro começa o intervalo de medição e o segundo recupera os resultados da medição.</span><span class="sxs-lookup"><span data-stu-id="dcc49-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dcc49-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcc49-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc49-131">APIs de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="dcc49-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



