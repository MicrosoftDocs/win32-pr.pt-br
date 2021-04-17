---
description: Codificação de taxa de bits variável irrestrita
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codificação de taxa de bits variável irrestrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811485"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="4f746-103">Codificação de taxa de bits variável irrestrita</span><span class="sxs-lookup"><span data-stu-id="4f746-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="4f746-104">No modo de codificação de taxa de bits variável (VBR) irrestrito, o conteúdo é codificado para a melhor qualidade possível, mantendo uma taxa de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="4f746-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="4f746-105">A codificação de VBR não restringida usa duas passagens de codificação.</span><span class="sxs-lookup"><span data-stu-id="4f746-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="4f746-106">Ao usar a codificação VBR não restringida, você especifica uma taxa de bits para o fluxo, como faria com a [codificação de taxa de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="4f746-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="4f746-107">No entanto, o codificador usa esse valor somente como a taxa de bits média para o fluxo e codifica para que a qualidade seja a mais alta possível, mantendo a média.</span><span class="sxs-lookup"><span data-stu-id="4f746-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="4f746-108">Exemplos individuais produzidos pelo codificador variam em tamanho sem nenhum limite de buffer explícito.</span><span class="sxs-lookup"><span data-stu-id="4f746-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="4f746-109">No entanto, a taxa de bits média durante a sessão de codificação e a duração do fluxo não devem ser mais do que o valor especificado por você.</span><span class="sxs-lookup"><span data-stu-id="4f746-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="4f746-110">A taxa de bits real em qualquer ponto no fluxo codificado pode variar muito do valor médio.</span><span class="sxs-lookup"><span data-stu-id="4f746-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="4f746-111">Você não define uma janela de buffer para a codificação de VBR não restringida.</span><span class="sxs-lookup"><span data-stu-id="4f746-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="4f746-112">Em vez disso, o codificador computa o tamanho da janela de buffer necessária com base nos requisitos dos exemplos codificados.</span><span class="sxs-lookup"><span data-stu-id="4f746-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="4f746-113">Isso significa que não há nenhum limite para o tamanho de amostras individuais no fluxo, desde que a taxa de bits média seja menor ou igual ao valor definido.</span><span class="sxs-lookup"><span data-stu-id="4f746-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="4f746-114">A vantagem da codificação de VBR não restringida é que o fluxo compactado tem a melhor qualidade possível enquanto permanece dentro de uma largura de banda média previsível.</span><span class="sxs-lookup"><span data-stu-id="4f746-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="4f746-115">Use isso quando precisar especificar uma largura de banda, mas flutuações em relação à largura de banda especificada são aceitáveis; por exemplo, para arquivos locais ou somente para download.</span><span class="sxs-lookup"><span data-stu-id="4f746-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="4f746-116">A desvantagem desse modo de codificação é que o codificador pode definir a janela de buffer para qualquer valor necessário após a codificação, dando-lhe nenhum controle sobre o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="4f746-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="4f746-117">Na maioria dos casos, se você não estiver preocupado com o tamanho do buffer ou a consistência do uso da largura de banda, use a [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)</span><span class="sxs-lookup"><span data-stu-id="4f746-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="4f746-118">Configurando o codificador para uma VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="4f746-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="4f746-119">A configuração do codificador é definida por meio de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="4f746-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="4f746-120">Essas propriedades são definidas em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="4f746-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="4f746-121">As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="4f746-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="4f746-122">Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4f746-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="4f746-123">Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída de VBR com suporte e selecionar o necessário no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT) com base na taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="4f746-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="4f746-124">A lista a seguir mostra as propriedades que você deve definir para esse tipo de codificação:</span><span class="sxs-lookup"><span data-stu-id="4f746-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="4f746-125">Especifique o modo de codificação de VBR definindo a \_ Propriedade MFPKEY VBRENABLED como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="4f746-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="4f746-126">Defina MFPKEY \_ PASSESUSED como 2 porque o modo VBR não restringido usa duas passagens de codificação.</span><span class="sxs-lookup"><span data-stu-id="4f746-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="4f746-127">Ao enumerar o tipo de mídia de saída, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de taxa de [**\_ \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4f746-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="4f746-128">Escolha um tipo de mídia de saída que tenha a taxa de bits média mais próxima da taxa de bits média desejada que você deseja que o codificador mantenha no conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="4f746-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="4f746-129">Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4f746-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="4f746-130">Para obter o valor da janela buffer é definido pelo codificador, chame **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido em wmcodecifaces. h e wmcodecdspuuid. lib, após a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="4f746-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="4f746-131">Para adicionar suporte de VBR não restringido para os fluxos, você deve definir esse valor no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores de Bucket de perda média) no objeto de configuração de fluxo ao configurar o perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="4f746-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="4f746-132">O seguinte modifica o método setencodingtype da classe de exemplo CEncoder para configurar o modo VBR não restringido.</span><span class="sxs-lookup"><span data-stu-id="4f746-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="4f746-133">Para obter informações sobre essa classe, consulte [código de exemplo do codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="4f746-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="4f746-134">Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte usando os exemplos de código de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4f746-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="4f746-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f746-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f746-136">Tipos de codificação ASF</span><span class="sxs-lookup"><span data-stu-id="4f746-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="4f746-137">O modelo de buffer de buckets vazados</span><span class="sxs-lookup"><span data-stu-id="4f746-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="4f746-138">Como criar uma topologia para Two-Pass a codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="4f746-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



