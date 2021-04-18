---
description: 'Na taxa de bits variável com restrição de pico (VBR), o conteúdo é codificado para uma taxa de bits especificada e valores de pico: uma taxa de bits de pico e uma janela de buffer de pico.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Codificação de taxa de bits de variável Peak-Constrained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766411"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="bae12-103">Codificação de taxa de bits de variável Peak-Constrained</span><span class="sxs-lookup"><span data-stu-id="bae12-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="bae12-104">Na taxa de bits variável com restrição de pico (VBR), o conteúdo é codificado para uma taxa de bits especificada e *valores de pico*: uma taxa de bits de pico e uma janela de buffer de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="bae12-105">Esses valores de pico também são chamados de *valores de Bucket de pico de vazamento*.</span><span class="sxs-lookup"><span data-stu-id="bae12-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="bae12-106">O arquivo é codificado para estar em conformidade com um buffer descrito pelos valores de pico, de modo que a taxa de bits média geral do fluxo seja igual ou menor que o valor médio de taxa de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="bae12-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="bae12-107">Normalmente, a taxa de bits de pico é muito alta.</span><span class="sxs-lookup"><span data-stu-id="bae12-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="bae12-108">O codificador garante que o valor de taxa de bits médio especificado seja mantido durante a duração do fluxo (taxa média de bits >= (tamanho total do fluxo em bits/duração do fluxo em segundos)).</span><span class="sxs-lookup"><span data-stu-id="bae12-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="bae12-109">Considere o exemplo a seguir: Configure um fluxo com uma taxa média de bits de 16.000 bits por segundo, uma taxa de bits de pico de 48.000 bits por segundo e uma janela de buffer de pico de 3.000 (3 segundos).</span><span class="sxs-lookup"><span data-stu-id="bae12-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="bae12-110">O tamanho do buffer usado para o fluxo é de 144.000 bits (48.000 bits por segundo \* 3 segundos) conforme determinado pelos valores de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="bae12-111">O codificador compacta os dados para que estejam em conformidade com esse buffer.</span><span class="sxs-lookup"><span data-stu-id="bae12-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="bae12-112">Além disso, a taxa média de bits do fluxo deve ser de 16.000 ou menos.</span><span class="sxs-lookup"><span data-stu-id="bae12-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="bae12-113">Se o codificador precisar criar amostras grandes para lidar com um segmento de conteúdo complexo, ele poderá aproveitar o tamanho do buffer grande.</span><span class="sxs-lookup"><span data-stu-id="bae12-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="bae12-114">Mas outras partes do fluxo devem ser codificadas em uma taxa de bits inferior para reduzir a média para o nível especificado.</span><span class="sxs-lookup"><span data-stu-id="bae12-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="bae12-115">A codificação de taxa de bits de pico restrita é útil para dispositivos de reprodução com uma capacidade de buffer finita e restrições de taxa de dados.</span><span class="sxs-lookup"><span data-stu-id="bae12-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="bae12-116">Um exemplo comum disso é a codificação usada para DVDs quando a decodificação é executada por um chip em um dispositivo, onde há limitações de hardware que devem ser consideradas.</span><span class="sxs-lookup"><span data-stu-id="bae12-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="bae12-117">Configurando o codificador para Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="bae12-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="bae12-118">A VBR com restrição de pico é como uma [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) não restrita, pois ela é confinada a uma taxa média de bits durante a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="bae12-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="bae12-119">Além disso, a taxa de bits com restrição de pico está em conformidade com um buffer de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="bae12-120">Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="bae12-121">Esse modo usa duas passagens de codificação e fornece a flexibilidade do codificador em como ele codifica exemplos individuais enquanto obedece às limitações de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="bae12-122">A configuração do codificador é definida por meio de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bae12-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="bae12-123">Essas propriedades são definidas em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="bae12-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="bae12-124">As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="bae12-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="bae12-125">Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bae12-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="bae12-126">Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída de VBR com suporte e selecionar o necessário no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT) com base na taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="bae12-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="bae12-127">Você deve definir o seguinte propertiesfor deste tipo de codificação:</span><span class="sxs-lookup"><span data-stu-id="bae12-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="bae12-128">Especifique o modo de codificação de VBR definindo a \_ Propriedade MFPKEY VBRENABLED como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="bae12-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="bae12-129">Defina MFPKEY \_ PASSESUSED como 2 porque o modo VBR com restrição de pico usa duas passagens de codificação.</span><span class="sxs-lookup"><span data-stu-id="bae12-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="bae12-130">Defina MFPKEY \_ RMAX para especificar a taxa de bits de pico e defina MFPKEY \_ BMAX para especificar a janela de pico do buffer.</span><span class="sxs-lookup"><span data-stu-id="bae12-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="bae12-131">Ao enumerar o tipo de mídia de saída, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de [**\_ \_ \_ taxa de bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis e escolha um tipo de mídia de saída que tenha a taxa de bits média mais próxima da taxa de bits média desejada que você deseja que</span><span class="sxs-lookup"><span data-stu-id="bae12-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="bae12-132">Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bae12-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="bae12-133">É recomendável que você defina a taxa de bits de pico para pelo menos duas vezes a taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="bae12-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="bae12-134">Definir a taxa de pico para um valor mais baixo pode fazer com que o codificador Codifique o conteúdo como CBR de duas passagens em vez da taxa de bits de pico restrita.</span><span class="sxs-lookup"><span data-stu-id="bae12-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="bae12-135">Para obter o valor da janela de buffer definido pelo codificador, chame **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido em wmcodecifaces. h, wmcodecdspuuid. lib, após a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="bae12-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="bae12-136">Para adicionar suporte de VBR não restringido para os fluxos, você deve definir esse valor no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (pico de vazamentos de Bucket) no objeto de configuração de fluxo ao configurar o perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="bae12-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="bae12-137">O exemplo de código a seguir modifica o método setencodingtype da classe de exemplo CEncoder para configurar o modo de taxa de bits restrita de pico.</span><span class="sxs-lookup"><span data-stu-id="bae12-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="bae12-138">Para obter informações sobre essa classe, consulte [código de exemplo do codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="bae12-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="bae12-139">Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte usando os exemplos de código de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bae12-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="bae12-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bae12-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae12-141">Tipos de codificação ASF</span><span class="sxs-lookup"><span data-stu-id="bae12-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="bae12-142">O modelo de buffer de buckets vazados</span><span class="sxs-lookup"><span data-stu-id="bae12-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="bae12-143">Como criar uma topologia para Two-Pass a codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="bae12-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



