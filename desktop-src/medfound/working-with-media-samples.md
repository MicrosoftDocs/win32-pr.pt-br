---
description: Trabalhando com exemplos de mídia
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Trabalhando com exemplos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930096"
---
# <a name="working-with-media-samples"></a>Trabalhando com exemplos de mídia

Este tópico descreve como usar a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para manipular objetos de exemplo de mídia. Para obter uma visão geral dos exemplos de mídia, consulte [amostras de mídia](media-samples.md).

Para criar um novo exemplo de mídia, chame a função [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) . Inicialmente, a lista de buffers do exemplo está vazia. Para adicionar um buffer ao final da lista, chame [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

O código a seguir mostra como criar um exemplo e adicionar um buffer a ele.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



A maneira recomendada para obter os buffers do exemplo é chamar [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Esse método retorna um único buffer continguous.

Para iterar pelos buffers na lista, comece chamando [**IMFSample:: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount). Esse método retorna o número de buffers. Em seguida, chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) e especifique o índice do buffer a ser recuperado. Os buffers são indexados de zero.

O código a seguir mostra como iterar pelos buffers em um exemplo.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Os exemplos têm um carimbo de data/hora e uma duração. O carimbo de data/hora indica quando os dados no exemplo devem ser renderizados, em relação ao relógio de apresentação. A duração é o período de tempo para o qual os dados devem ser renderizados. Normalmente, o componente que gera os dados define o carimbo de data/hora inicial e a duração. Esses valores podem ser modificados pela sessão de mídia. Para definir o carimbo de data/hora, chame [**IMFSample:: Setamostratime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Para definir a duração, chame [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Os exemplos também podem ter atributos, que contêm informações adicionais sobre o exemplo. Para obter uma lista de atributos de exemplo, consulte [atributos de exemplo](sample-attributes.md). Para definir e recuperar atributos, use a [**interface IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), que o [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) herda.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras de mídia](media-samples.md)
</dt> <dt>

[Buffers de mídia](media-buffers.md)
</dt> </dl>

 

 



