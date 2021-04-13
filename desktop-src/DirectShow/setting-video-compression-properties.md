---
description: Definindo propriedades de compactação de vídeo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Definindo propriedades de compactação de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370227"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="ea718-103">Definindo propriedades de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ea718-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="ea718-104">Os filtros de compactação de vídeo podem dar suporte à interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) em seus PINs de saída.</span><span class="sxs-lookup"><span data-stu-id="ea718-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="ea718-105">Use essa interface para definir propriedades de compactação, como a taxa de quadros-chave, o número de quadros previstos (P) por quadro-chave e a qualidade de compactação relativa.</span><span class="sxs-lookup"><span data-stu-id="ea718-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="ea718-106">Primeiro, chame o método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para localizar o PIN de saída do filtro e consulte o PIN da interface.</span><span class="sxs-lookup"><span data-stu-id="ea718-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="ea718-107">Alguns filtros podem não dar suporte à interface.</span><span class="sxs-lookup"><span data-stu-id="ea718-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="ea718-108">Outros podem expor a interface, mas não oferecem suporte a todas as propriedades de compactação.</span><span class="sxs-lookup"><span data-stu-id="ea718-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="ea718-109">Para determinar quais propriedades têm suporte, chame [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="ea718-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="ea718-110">Esse método retorna várias informações:</span><span class="sxs-lookup"><span data-stu-id="ea718-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="ea718-111">Um conjunto de sinalizadores de recursos</span><span class="sxs-lookup"><span data-stu-id="ea718-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="ea718-112">Uma cadeia de caracteres descritiva e uma cadeia de número de versão</span><span class="sxs-lookup"><span data-stu-id="ea718-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="ea718-113">Valores padrão para a taxa de quadros chave, a taxa de quadros P e a qualidade (quando há suporte)</span><span class="sxs-lookup"><span data-stu-id="ea718-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="ea718-114">O método tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ea718-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="ea718-115">Os parâmetros *pszVersion* e *pszDesc* são buffers de caracteres largos que recebem a cadeia de caracteres da versão e a cadeia de caracteres de descrição.</span><span class="sxs-lookup"><span data-stu-id="ea718-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="ea718-116">Os parâmetros *cbVersion* e *cbDesc* recebem os tamanhos de buffer necessários em bytes (não caracteres).</span><span class="sxs-lookup"><span data-stu-id="ea718-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="ea718-117">Os parâmetros *lKeyFrame*, *lPFrame* e *dblQuality* recebem os valores padrão para a taxa de quadros-chave, a taxa de quadros P e a qualidade.</span><span class="sxs-lookup"><span data-stu-id="ea718-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="ea718-118">A qualidade é expressa como um número de ponto flutuante de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="ea718-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="ea718-119">O parâmetro *lCap* recebe um **ou** bit-a de flags de recursos, que são definidos pelo tipo enumerado [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .</span><span class="sxs-lookup"><span data-stu-id="ea718-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="ea718-120">Qualquer um desses parâmetros pode ser **nulo** e, nesse caso, o método ignora esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ea718-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="ea718-121">Por exemplo, para alocar buffers para a versão e as cadeias de caracteres de descrição, primeiro chame o método com **NULL** no primeiro e no terceiro parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea718-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="ea718-122">Use os valores retornados para *cbVersion* e *cbDesc* para alocar os buffers e, em seguida, chame o método novamente:</span><span class="sxs-lookup"><span data-stu-id="ea718-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="ea718-123">O valor de *lCap* indica para quais dos outros métodos **IAMVideoCompression** o filtro dá suporte.</span><span class="sxs-lookup"><span data-stu-id="ea718-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="ea718-124">Por exemplo, se *lCap* contiver o \_ sinalizador nokeyframe CompressionCaps, você poderá chamar [**IAMVideoCompression:: \_ Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) dataframe para obter a taxa de quadros-chave e [**IAMVideoCompression::p UT \_**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) Key para definir a taxa de quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="ea718-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="ea718-125">Um valor negativo indica que o filtro usará o valor padrão, conforme Obtido em [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="ea718-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="ea718-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ea718-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="ea718-127">O exemplo de código a seguir tenta localizar a interface **IAMVideoCompression** no pino de saída.</span><span class="sxs-lookup"><span data-stu-id="ea718-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="ea718-128">Se tiver sucesso, ele recuperará os valores padrão e reais das propriedades de compactação:</span><span class="sxs-lookup"><span data-stu-id="ea718-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="ea718-129">Se você estiver usando a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para criar seu grafo, poderá obter a interface **IAMVideoCompression** chamando [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), em vez de usar **IBaseFilter:: EnumPins**.</span><span class="sxs-lookup"><span data-stu-id="ea718-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="ea718-130">O método **FindInterface** é um método auxiliar que pesquisa filtros e Pins no grafo para uma interface especificada.</span><span class="sxs-lookup"><span data-stu-id="ea718-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



