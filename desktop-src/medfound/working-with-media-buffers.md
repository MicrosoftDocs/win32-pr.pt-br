---
description: Trabalhando com buffers de mídia
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Trabalhando com buffers de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837652"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="2e2e4-103">Trabalhando com buffers de mídia (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="2e2e4-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2e2e4-104">Este tópico descreve como usar a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) para acessar os dados em um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="2e2e4-105">Todos os buffers de mídia expõem **IMFMediaBuffer**, que é projetado para qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="2e2e4-106">Quadros de vídeo descompactados são um caso especial, descritos no tópico [buffers de vídeo descompactados](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="2e2e4-107">Tamanho do Buffer</span><span class="sxs-lookup"><span data-stu-id="2e2e4-107">Buffer Size</span></span>

<span data-ttu-id="2e2e4-108">Um buffer de mídia tem dois tamanhos associados a ele:</span><span class="sxs-lookup"><span data-stu-id="2e2e4-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="2e2e4-109">O *comprimento máximo* é o tamanho físico da memória que é alocada para o buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="2e2e4-110">Esse valor é definido quando o buffer é criado e não é alterado durante o tempo de vida do buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="2e2e4-111">O comprimento máximo indica a quantidade de dados que pode ser armazenada no buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="2e2e4-112">Para localizar o tamanho máximo, chame [**IMFMediaBuffer:: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="2e2e4-113">O *comprimento atual* é a quantidade de dados válidos que estão atualmente no buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="2e2e4-114">Quando o buffer é alocado pela primeira vez, o comprimento atual é zero, porque não há dados válidos no buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="2e2e4-115">Se você gravar dados no buffer, deverá atualizar o comprimento atual chamando [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="2e2e4-116">Por exemplo, se você gravar 100 bytes de dados no buffer, chame **SetCurrentLength** com o valor 100.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="2e2e4-117">Se você ler dados de um buffer de mídia, chame [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) para descobrir a quantidade de dados atualmente no buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="2e2e4-118">Não ler após o comprimento atual.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-118">Do not read past the current length.</span></span> <span data-ttu-id="2e2e4-119">O comprimento atual nunca pode exceder o comprimento máximo do buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="2e2e4-120">Acessando a memória de buffer</span><span class="sxs-lookup"><span data-stu-id="2e2e4-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="2e2e4-121">Para acessar a memória no buffer, chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="2e2e4-122">Esse método retorna um ponteiro para o início do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="2e2e4-123">Ele também retorna o comprimento máximo e o comprimento atual.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="2e2e4-124">Quando terminar de usar o ponteiro, chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="2e2e4-125">Para gravar dados em um buffer de mídia:</span><span class="sxs-lookup"><span data-stu-id="2e2e4-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="2e2e4-126">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="2e2e4-127">O método também retorna o comprimento máximo do buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="2e2e4-128">Grave seus dados na memória, até o comprimento máximo do buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="2e2e4-129">Chame [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) para atualizar o comprimento atual.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="2e2e4-130">Defina o comprimento atual igual à quantidade de dados que você escreveu na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="2e2e4-131">Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="2e2e4-132">Para ler dados de um buffer de mídia:</span><span class="sxs-lookup"><span data-stu-id="2e2e4-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="2e2e4-133">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="2e2e4-134">O método também retorna o comprimento atual do buffer (a quantidade de dados válidos no buffer).</span><span class="sxs-lookup"><span data-stu-id="2e2e4-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="2e2e4-135">Ler o conteúdo da memória, até o comprimento atual.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="2e2e4-136">Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="2e2e4-137">Criando buffers de memória do sistema</span><span class="sxs-lookup"><span data-stu-id="2e2e4-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="2e2e4-138">O buffer de memória do sistema é um buffer de mídia que gerencia um bloco de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="2e2e4-139">Para criar uma instância desse objeto, chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ou [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) e especifique um tamanho de buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="2e2e4-140">Ambas as funções alocam um bloco de memória e retornam um ponteiro [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2e2e4-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="2e2e4-141">A memória é liberada automaticamente quando a contagem de referência do buffer de mídia atinge zero e o objeto é destruído.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="2e2e4-142">O exemplo a seguir mostra como criar um buffer de memória do sistema e gravar no buffer.</span><span class="sxs-lookup"><span data-stu-id="2e2e4-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2e2e4-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e2e4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e2e4-144">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="2e2e4-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="2e2e4-145">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e2e4-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



