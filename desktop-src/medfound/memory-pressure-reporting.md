---
description: O relatório de pressão de memória permite que um aplicativo Direct3D determine quando seu conjunto de trabalho de memória de vídeo ficou muito grande.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Relatório de pressão de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723766"
---
# <a name="memory-pressure-reporting"></a>Relatório de pressão de memória

O relatório de pressão de memória permite que um aplicativo Direct3D determine quando seu conjunto de trabalho de memória de vídeo ficou muito grande.

*A pressão de* memória é a demanda colocada no subsistema de memória por um aplicativo. Embora qualquer aplicativo Direct3D possa usar relatórios de pressão de memória, esse recurso é especialmente útil para aplicativos que renderizam vídeo usando o Direct3D. A reprodução de vídeo normalmente se beneficia de grandes quantidades de buffer, para que os quadros possam ser decodificados com antecedência. Embora o buffer geralmente resulta em reprodução mais suave, ele pode realmente prejudicar o desempenho se o conjunto de trabalho cresce muito grande, devido aos seguintes fatores:

-   A memória pode ser despejada do cache. Na pior das hipóteses, isso pode ocorrer em cada quadro de vídeo.
-   As alocações de memória podem ser colocadas em segmentos de memória não ideal.

A partir do Windows 7, o Direct3D pode relatar algumas estatísticas sobre a pressão de memória de vídeo:

-   O número de bytes despejados pelo processo em um intervalo de tempo.
-   A quantidade de memória colocada em segmentos de memória não ideal.
-   Uma indicação aproximada da eficiência geral das alocações de memória colocadas na memória não ideal.

Essas informações podem ajudar um aplicativo a manter um conjunto de trabalho razoável.

## <a name="using-memory-pressure-reporting"></a>Usando relatórios de pressão de memória

O relatório de pressão de memória usa a interface **IDirect3DQuery9** existente para consultar o dispositivo. Um novo tipo de consulta foi adicionado à **enumeração D3DQUERYTYPE.**


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Para usar essa consulta, execute as seguintes etapas:

1.  Chame **IDirect3DDevice9Ex::CreateQuery** com o **sinalizador D3DQUERYTYPE \_ MEMORYPRESSURE.** Esse método retorna um ponteiro para a interface **IDirect3DQuery9.**
2.  Chame **IDirect3DQuery9::Issue** com o sinalizador **D3DISSUE \_ BEGIN** para iniciar o intervalo de medição.
3.  Chame **IDirect3DQuery9::Issue** com o **sinalizador D3DISSUE \_ END.**
4.  Chame **IDirect3DQuery9::GetData** para obter o resultado da consulta. A consulta retorna uma [**estrutura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra duas funções que medem a pressão de memória. O primeiro inicia o intervalo de medição e o segundo recupera os resultados da medida.


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

 

 



