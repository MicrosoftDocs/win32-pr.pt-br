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
# <a name="memory-pressure-reporting"></a>Relatório de pressão de memória

O relatório de demanda de memória permite que um aplicativo do Direct3D determine quando seu conjunto de trabalho de memória de vídeo cresceu muito grande.

A *pressão de memória* é a demanda colocada no subsistema de memória por um aplicativo. Embora qualquer aplicativo Direct3D possa usar o relatório de pressão de memória, esse recurso é especialmente útil para aplicativos que renderizam vídeo usando o Direct3D. A reprodução de vídeo normalmente se beneficia de grandes quantidades de buffer, para que os quadros possam ser decodificados antecipadamente. Embora o armazenamento em buffer geralmente resulte em uma reprodução mais suave, isso pode prejudicar o desempenho se o conjunto de trabalho ficar muito grande, devido aos seguintes fatores:

-   A memória pode ser removida do cache. Na pior das hipóteses, isso pode ocorrer em cada quadro de vídeo.
-   As alocações de memória podem ser colocadas em segmentos de memória não ideais.

A partir do Windows 7, o Direct3D pode relatar algumas estatísticas sobre a pressão da memória de vídeo:

-   O número de bytes removidos pelo processo durante um intervalo de tempo.
-   A quantidade de memória colocada em segmentos de memória não ideais.
-   Uma indicação aproximada da eficiência geral das alocações de memória colocadas na memória não ideal.

Essas informações podem ajudar um aplicativo a manter um conjunto de trabalho razoável.

## <a name="using-memory-pressure-reporting"></a>Usando o relatório de pressão de memória

O relatório de demanda de memória usa a interface **IDirect3DQuery9** existente para consultar o dispositivo. Um novo tipo de consulta foi adicionado à enumeração **D3DQUERYTYPE** .


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Para usar essa consulta, execute as seguintes etapas:

1.  Chame **IDirect3DDevice9Ex:: CreateQuery** com o sinalizador **D3DQUERYTYPE \_ MEMORYPRESSURE** . Esse método retorna um ponteiro para a interface **IDirect3DQuery9** .
2.  Chame **IDirect3DQuery9:: Issue** com o sinalizador de **\_ início D3DISSUE** para iniciar o intervalo de medição.
3.  Chame **IDirect3DQuery9:: Issue** com o sinalizador de **\_ finalização de D3DISSUE** .
4.  Chame **IDirect3DQuery9:: GetData** para obter o resultado da consulta. A consulta retorna uma estrutura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra duas funções que medem a pressão de memória. O primeiro começa o intervalo de medição e o segundo recupera os resultados da medição.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



