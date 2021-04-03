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
# <a name="working-with-media-samples"></a><span data-ttu-id="09a1f-103">Trabalhando com exemplos de mídia</span><span class="sxs-lookup"><span data-stu-id="09a1f-103">Working with Media Samples</span></span>

<span data-ttu-id="09a1f-104">Este tópico descreve como usar a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para manipular objetos de exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="09a1f-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="09a1f-105">Para obter uma visão geral dos exemplos de mídia, consulte [amostras de mídia](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="09a1f-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="09a1f-106">Para criar um novo exemplo de mídia, chame a função [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) .</span><span class="sxs-lookup"><span data-stu-id="09a1f-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="09a1f-107">Inicialmente, a lista de buffers do exemplo está vazia.</span><span class="sxs-lookup"><span data-stu-id="09a1f-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="09a1f-108">Para adicionar um buffer ao final da lista, chame [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="09a1f-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="09a1f-109">O código a seguir mostra como criar um exemplo e adicionar um buffer a ele.</span><span class="sxs-lookup"><span data-stu-id="09a1f-109">The following code shows how to create a sample and add a buffer to it.</span></span>


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



<span data-ttu-id="09a1f-110">A maneira recomendada para obter os buffers do exemplo é chamar [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span><span class="sxs-lookup"><span data-stu-id="09a1f-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="09a1f-111">Esse método retorna um único buffer continguous.</span><span class="sxs-lookup"><span data-stu-id="09a1f-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="09a1f-112">Para iterar pelos buffers na lista, comece chamando [**IMFSample:: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span><span class="sxs-lookup"><span data-stu-id="09a1f-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="09a1f-113">Esse método retorna o número de buffers.</span><span class="sxs-lookup"><span data-stu-id="09a1f-113">This method returns the number of buffers.</span></span> <span data-ttu-id="09a1f-114">Em seguida, chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) e especifique o índice do buffer a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="09a1f-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="09a1f-115">Os buffers são indexados de zero.</span><span class="sxs-lookup"><span data-stu-id="09a1f-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="09a1f-116">O código a seguir mostra como iterar pelos buffers em um exemplo.</span><span class="sxs-lookup"><span data-stu-id="09a1f-116">The following code shows how to iterate through the buffers in a sample.</span></span>


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



<span data-ttu-id="09a1f-117">Os exemplos têm um carimbo de data/hora e uma duração.</span><span class="sxs-lookup"><span data-stu-id="09a1f-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="09a1f-118">O carimbo de data/hora indica quando os dados no exemplo devem ser renderizados, em relação ao relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="09a1f-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="09a1f-119">A duração é o período de tempo para o qual os dados devem ser renderizados.</span><span class="sxs-lookup"><span data-stu-id="09a1f-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="09a1f-120">Normalmente, o componente que gera os dados define o carimbo de data/hora inicial e a duração.</span><span class="sxs-lookup"><span data-stu-id="09a1f-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="09a1f-121">Esses valores podem ser modificados pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="09a1f-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="09a1f-122">Para definir o carimbo de data/hora, chame [**IMFSample:: Setamostratime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="09a1f-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="09a1f-123">Para definir a duração, chame [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="09a1f-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="09a1f-124">Os exemplos também podem ter atributos, que contêm informações adicionais sobre o exemplo.</span><span class="sxs-lookup"><span data-stu-id="09a1f-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="09a1f-125">Para obter uma lista de atributos de exemplo, consulte [atributos de exemplo](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="09a1f-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="09a1f-126">Para definir e recuperar atributos, use a [**interface IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), que o [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) herda.</span><span class="sxs-lookup"><span data-stu-id="09a1f-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09a1f-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09a1f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a1f-128">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="09a1f-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="09a1f-129">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="09a1f-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



