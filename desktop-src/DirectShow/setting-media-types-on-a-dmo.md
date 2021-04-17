---
description: Definindo tipos de mídia em um DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Definindo tipos de mídia em um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782835"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="c22b5-103">Definindo tipos de mídia em um DMO</span><span class="sxs-lookup"><span data-stu-id="c22b5-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="c22b5-104">Antes que um DMO possa processar quaisquer dados, o cliente deve definir o tipo de mídia para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="c22b5-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="c22b5-105">(Há uma exceção secundária para essa regra; consulte [fluxos opcionais](optional-streams.md).) Para localizar o número de fluxos, chame o método [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :</span><span class="sxs-lookup"><span data-stu-id="c22b5-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="c22b5-106">Esse método retorna dois valores, o número de entradas e o número de saídas.</span><span class="sxs-lookup"><span data-stu-id="c22b5-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="c22b5-107">Esses valores são fixos para o tempo de vida do DMO.</span><span class="sxs-lookup"><span data-stu-id="c22b5-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="c22b5-108">**Tipos preferenciais**</span><span class="sxs-lookup"><span data-stu-id="c22b5-108">**Preferred Types**</span></span>

<span data-ttu-id="c22b5-109">Para cada fluxo, o DMO atribui uma lista de tipos de mídia possíveis, em ordem de preferência.</span><span class="sxs-lookup"><span data-stu-id="c22b5-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="c22b5-110">Por exemplo, os tipos preferenciais podem ser 32-RGB, RGB de 24 bits e RGB de 16 bits, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="c22b5-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="c22b5-111">Quando o cliente define os tipos de mídia, ele pode usar essas listas como uma dica.</span><span class="sxs-lookup"><span data-stu-id="c22b5-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="c22b5-112">Para recuperar um tipo preferencial para um fluxo, chame o método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) ou [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="c22b5-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="c22b5-113">Especifique o número do fluxo e um valor de índice para o tipo (começando de zero).</span><span class="sxs-lookup"><span data-stu-id="c22b5-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="c22b5-114">Por exemplo, o código a seguir recupera o primeiro tipo preferencial do primeiro fluxo de entrada:</span><span class="sxs-lookup"><span data-stu-id="c22b5-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="c22b5-115">Para enumerar todos os tipos de mídia preferenciais em um determinado fluxo, use um loop que incrementa o índice de tipo até que o método retorne DMO \_ E \_ não \_ mais \_ itens, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="c22b5-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="c22b5-116">Você deve observar os seguintes pontos sobre os tipos preferenciais:</span><span class="sxs-lookup"><span data-stu-id="c22b5-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="c22b5-117">O DMO pode retornar um tipo que não tem nenhum bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="c22b5-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="c22b5-118">Por exemplo, um DMO poderia especificar um tipo de vídeo, como RGB de 24 bits, sem fornecer a largura e a altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="c22b5-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="c22b5-119">No entanto, quando você define o tipo, deve fornecer um bloco de formato completo.</span><span class="sxs-lookup"><span data-stu-id="c22b5-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="c22b5-120">(Alguns tipos de mídia, como MIDI, nunca exigem um bloco de formato; nesse caso, esse comentário não se aplica.)</span><span class="sxs-lookup"><span data-stu-id="c22b5-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="c22b5-121">O DMO não é necessário para dar suporte a cada combinação de tipos preferenciais que ele retorna.</span><span class="sxs-lookup"><span data-stu-id="c22b5-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="c22b5-122">Por exemplo, se um DMO tiver dois fluxos, e cada fluxo tiver quatro tipos preferenciais, haverá 16 combinações possíveis, mas nem todos eles terão a garantia de serem válidos.</span><span class="sxs-lookup"><span data-stu-id="c22b5-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="c22b5-123">Quando o cliente define o tipo de mídia para um fluxo, o DMO pode atualizar os tipos preferenciais para outros fluxos para refletir o novo estado.</span><span class="sxs-lookup"><span data-stu-id="c22b5-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="c22b5-124">No entanto, não é necessário fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c22b5-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="c22b5-125">Para alguns fluxos, o DMO pode não oferecer nenhum tipo preferencial.</span><span class="sxs-lookup"><span data-stu-id="c22b5-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="c22b5-126">Normalmente, um DMO deve oferecer pelo menos alguns tipos preferenciais em alguns fluxos.</span><span class="sxs-lookup"><span data-stu-id="c22b5-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="c22b5-127">O DMO não precisa oferecer uma lista completa dos tipos de mídia que ele pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="c22b5-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="c22b5-128">Pode haver tipos "não anunciados" que o DMO dá suporte, mas não oferece como tipos preferenciais.</span><span class="sxs-lookup"><span data-stu-id="c22b5-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="c22b5-129">Em suma, o cliente deve tratar os tipos preferenciais como somente diretrizes.</span><span class="sxs-lookup"><span data-stu-id="c22b5-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="c22b5-130">A única maneira de saber quais tipos têm suporte é testá-los, conforme descrito na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="c22b5-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="c22b5-131">**Configurando o tipo de mídia em um fluxo**</span><span class="sxs-lookup"><span data-stu-id="c22b5-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="c22b5-132">Use os métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o tipo para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="c22b5-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="c22b5-133">Você deve fornecer uma estrutura de **\_ \_ tipo de mídia DMO** que contém uma descrição completa do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c22b5-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="c22b5-134">O exemplo a seguir define o tipo de mídia no fluxo de entrada 0, usando áudio PCM estéreo de 16 bits de 44,1-kHz:</span><span class="sxs-lookup"><span data-stu-id="c22b5-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="c22b5-135">Para testar um tipo de mídia sem defini-lo, chame **SetInputType** ou **setoutputtypetype** com o \_ sinalizador do set \_ TYPEF \_ test \_ only.</span><span class="sxs-lookup"><span data-stu-id="c22b5-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="c22b5-136">O método retornará S \_ OK se o tipo for aceitável ou, \_ caso contrário, s false:</span><span class="sxs-lookup"><span data-stu-id="c22b5-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="c22b5-137">Como as configurações em um fluxo podem afetar outro fluxo, talvez seja necessário limpar o tipo de mídia de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="c22b5-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="c22b5-138">Para fazer isso, chame **SetInputType** ou **setoutputtypetype** com o \_ sinalizador Set \_ TYPEF \_ Clear do DMO.</span><span class="sxs-lookup"><span data-stu-id="c22b5-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="c22b5-139">Para um decodificador DMO, o cliente normalmente definiria o tipo de entrada primeiro e, em seguida, escolheria um tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="c22b5-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="c22b5-140">Para um codificador DMO, o cliente definiria o tipo de saída primeiro e, em seguida, o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c22b5-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22b5-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c22b5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22b5-142">Hospedando diretamente um DMO</span><span class="sxs-lookup"><span data-stu-id="c22b5-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



