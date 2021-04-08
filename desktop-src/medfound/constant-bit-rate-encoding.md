---
description: Codificação de taxa de bits constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codificação de taxa de bits constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920633"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="96b7c-103">Codificação de taxa de bits constante</span><span class="sxs-lookup"><span data-stu-id="96b7c-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="96b7c-104">Em codificação de taxa de bits constante (CBR), o codificador sabe a taxa de bits dos exemplos de mídia de saída e a janela de buffer (parâmetros de Bucket de vazamento) antes do início da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="96b7c-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="96b7c-105">O codificador usa o mesmo número de bits para codificar cada segundo de amostra durante a duração do arquivo para atingir a taxa de bits de destino para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="96b7c-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="96b7c-106">Isso limita a variação no tamanho dos exemplos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="96b7c-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="96b7c-107">Além disso, durante a sessão de codificação, a taxa de bits não está exatamente no valor especificado, mas permanece próxima da taxa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="96b7c-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="96b7c-108">A codificação CBR é útil quando você quer saber a taxa de bits ou a duração aproximada de um arquivo sem analisar o arquivo inteiro.</span><span class="sxs-lookup"><span data-stu-id="96b7c-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="96b7c-109">Isso é necessário em cenários de streaming ao vivo, em que o conteúdo de mídia precisa ser transmitido a uma taxa de bits previsível e com o uso de banda larga consistente.</span><span class="sxs-lookup"><span data-stu-id="96b7c-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="96b7c-110">A desvantagem da codificação CBR é que a qualidade do conteúdo codificado não será constante.</span><span class="sxs-lookup"><span data-stu-id="96b7c-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="96b7c-111">Como algum conteúdo é mais difícil de ser compactado, partes de um fluxo de CBR serão de menor qualidade do que outras.</span><span class="sxs-lookup"><span data-stu-id="96b7c-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="96b7c-112">Por exemplo, um filme típico tem algumas cenas que são razoavelmente estáticas e algumas cenas que estão cheias de ação.</span><span class="sxs-lookup"><span data-stu-id="96b7c-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="96b7c-113">Se você codificar um filme usando CBR, os bastidores que são estáticos e, portanto, fáceis de codificar com eficiência, serão de maior qualidade do que as cenas de ação, o que exigiria tamanhos de amostra mais altos para manter a mesma qualidade.</span><span class="sxs-lookup"><span data-stu-id="96b7c-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="96b7c-114">Em geral, as variações na qualidade de um arquivo CBR são mais pronunciadas em taxas de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="96b7c-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="96b7c-115">Em taxas de bits mais altas, a qualidade de um arquivo codificado em CBR ainda variará, mas os problemas de qualidade serão menos perceptíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="96b7c-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="96b7c-116">Ao usar a codificação de CBR, você deve definir a largura de banda tão alta quanto o cenário de entrega permitir.</span><span class="sxs-lookup"><span data-stu-id="96b7c-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="96b7c-117">Parâmetros de configuração da CBR</span><span class="sxs-lookup"><span data-stu-id="96b7c-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="96b7c-118">Configurações de Bucket de vazamento</span><span class="sxs-lookup"><span data-stu-id="96b7c-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="96b7c-119">Parâmetros de configuração da CBR</span><span class="sxs-lookup"><span data-stu-id="96b7c-119">CBR Configuration Settings</span></span>

<span data-ttu-id="96b7c-120">Você deve configurar um codificador especificando o tipo de codificação e as várias configurações específicas de fluxo antes da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="96b7c-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="96b7c-121">**Para configurar o codificador para a codificação CBR**</span><span class="sxs-lookup"><span data-stu-id="96b7c-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="96b7c-122">Especifique o modo de codificação de CBR.</span><span class="sxs-lookup"><span data-stu-id="96b7c-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="96b7c-123">Por padrão, o codificador está configurado para usar a codificação CBR.</span><span class="sxs-lookup"><span data-stu-id="96b7c-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="96b7c-124">A configuração do codificador é definida por meio de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="96b7c-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="96b7c-125">Essas propriedades são definidas em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="96b7c-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="96b7c-126">Você pode especificar esse modo explicitamente definindo a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="96b7c-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="96b7c-127">Para obter informações sobre como definir propriedades em codificadores, consulte [Configurando o codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="96b7c-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="96b7c-128">Escolha a taxa de bits de codificação.</span><span class="sxs-lookup"><span data-stu-id="96b7c-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="96b7c-129">Para a codificação de CBR, você deve saber a taxa de bits na qual deseja codificar o fluxo antes do início da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="96b7c-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="96b7c-130">Você deve definir a taxa de bits durante enquanto estiver configurando o codificador.</span><span class="sxs-lookup"><span data-stu-id="96b7c-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="96b7c-131">Para fazer isso, enquanto você estiver executando a negociação de tipo de mídia, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de [**\_ \_ \_ taxa de bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis e escolha um tipo de mídia de saída que tenha a taxa média de bits mais próxima da taxa de bit de</span><span class="sxs-lookup"><span data-stu-id="96b7c-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="96b7c-132">Para obter mais informações, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="96b7c-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="96b7c-133">O exemplo de código a seguir mostra a implementação de setencodingproperties.</span><span class="sxs-lookup"><span data-stu-id="96b7c-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="96b7c-134">Essa função define as propriedades de codificação de nível de fluxo para CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="96b7c-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="96b7c-135">Configurações de Bucket de vazamento</span><span class="sxs-lookup"><span data-stu-id="96b7c-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="96b7c-136">Para a codificação de CBR, a média e o máximo de valores de Bucket de vazamento para o fluxo são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="96b7c-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="96b7c-137">Para obter mais informações sobre esses parâmetros, consulte [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="96b7c-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="96b7c-138">Para codificar os fluxos de áudio de CBR, você precisa definir os valores de Bucket de vazamento depois de negociar o tipo de mídia de saída no codificador.</span><span class="sxs-lookup"><span data-stu-id="96b7c-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="96b7c-139">O codificador calcula a janela de buffer internamente com base na taxa média de bits definida no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="96b7c-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="96b7c-140">Para definir valores de Bucket de vazamento, crie uma matriz de DWORDs pode definir os valores a seguir na propriedade [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK corrigida MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) no repositório de propriedades do coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="96b7c-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="96b7c-141">Para obter mais informações, consulte [definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="96b7c-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="96b7c-142">Taxa média de bits: Obtenha a taxa média de bits do tipo de mídia de saída selecionado durante a negociação do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="96b7c-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="96b7c-143">Use o atributo de [**\_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="96b7c-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="96b7c-144">Janela buffer: consulte o codificador para a interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e, em seguida, chame [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).</span><span class="sxs-lookup"><span data-stu-id="96b7c-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="96b7c-145">Tamanho do buffer inicial: Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="96b7c-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96b7c-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96b7c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b7c-147">Tipos de codificação ASF</span><span class="sxs-lookup"><span data-stu-id="96b7c-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="96b7c-148">Tutorial: 1-transmitir codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="96b7c-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="96b7c-149">Tutorial: gravando um arquivo WMA usando a codificação de CBR</span><span class="sxs-lookup"><span data-stu-id="96b7c-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
