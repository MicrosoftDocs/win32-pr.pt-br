---
description: Codificação de taxa de bits de variável Quality-Based
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Codificação de taxa de bits de variável Quality-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783755"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="660a9-103">Codificação de taxa de bits de variável Quality-Based</span><span class="sxs-lookup"><span data-stu-id="660a9-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="660a9-104">Ao contrário da constante CBR ( [codificação de taxa de bits](constant-bit-rate-encoding.md) ), em que o codificador se esforça para manter uma taxa de bits específica da mídia codificada, no modo de taxa de bits variável (VBR), o codificador se esforça para obter a melhor qualidade possível da mídia codificada.</span><span class="sxs-lookup"><span data-stu-id="660a9-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="660a9-105">A principal diferença entre CBR e VBR é o tamanho da janela de buffer usada.</span><span class="sxs-lookup"><span data-stu-id="660a9-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="660a9-106">Fluxos de taxa de bits codificados geralmente têm janelas de buffer grandes em comparação com os fluxos codificados em CBR.</span><span class="sxs-lookup"><span data-stu-id="660a9-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="660a9-107">A qualidade do conteúdo codificado é determinada pela quantidade de dados que é perdida quando o conteúdo é compactado.</span><span class="sxs-lookup"><span data-stu-id="660a9-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="660a9-108">Muitos fatores afetam a perda de dados no processo de compactação; Mas, em geral, quanto mais complexos os dados originais e maior a taxa de compactação, mais detalhes serão perdidos no processo de compactação.</span><span class="sxs-lookup"><span data-stu-id="660a9-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="660a9-109">No modo VBR com base em qualidade, você não define uma taxa de bits ou uma janela de buffer que o codificador deve seguir.</span><span class="sxs-lookup"><span data-stu-id="660a9-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="660a9-110">Em vez disso, você especifica um nível de qualidade para um fluxo de mídia digital em vez de uma taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="660a9-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="660a9-111">O codificador compacta o conteúdo para que todos os exemplos sejam de qualidade comparável; Isso garante que a qualidade seja consistente durante toda a duração da reprodução, independentemente dos requisitos de buffer do fluxo resultante.</span><span class="sxs-lookup"><span data-stu-id="660a9-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="660a9-112">A codificação VBR baseada em qualidade tende a criar grandes fluxos compactados.</span><span class="sxs-lookup"><span data-stu-id="660a9-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="660a9-113">Em geral, esse tipo de codificação é adequado para reprodução local ou conexões de rede de largura de banda alta (ou download e reprodução).</span><span class="sxs-lookup"><span data-stu-id="660a9-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="660a9-114">Por exemplo, você pode escrever um aplicativo para copiar músicas de CD para arquivos ASF em um computador.</span><span class="sxs-lookup"><span data-stu-id="660a9-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="660a9-115">O uso da codificação VBR com base na qualidade garantiria que todas as músicas copiadas tenham a mesma qualidade.</span><span class="sxs-lookup"><span data-stu-id="660a9-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="660a9-116">Nesses casos, a qualidade consistente oferecerá uma melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="660a9-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="660a9-117">A desvantagem da codificação de VBR baseada em qualidade é que não há realmente nenhuma maneira de saber os requisitos de tamanho ou largura de banda da mídia codificada antes da sessão de codificação, pois o codificador usa uma única passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="660a9-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="660a9-118">Isso pode tornar arquivos codificados em taxa de bits com base em qualidade inadequados para circunstâncias em que a memória ou a largura de banda são restritas, como a reprodução de conteúdo em players de mídia portáteis ou streaming por uma rede de baixa largura de banda</span><span class="sxs-lookup"><span data-stu-id="660a9-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="660a9-119">Configurando o codificador para Quality-Based codificação de VBR</span><span class="sxs-lookup"><span data-stu-id="660a9-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="660a9-120">A configuração do codificador é definida por meio de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="660a9-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="660a9-121">Essas propriedades são definidas em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="660a9-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="660a9-122">As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="660a9-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="660a9-123">Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="660a9-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="660a9-124">A lista a seguir mostra as propriedades que você deve definir para esse tipo de codificação:</span><span class="sxs-lookup"><span data-stu-id="660a9-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="660a9-125">Especifique o modo de codificação de VBR definindo a propriedade **MFPKEY \_ VBRENABLED** como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="660a9-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="660a9-126">Defina **MFPKEY \_ PASSESUSED** como 1 porque esse modo VBR usa uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="660a9-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="660a9-127">Defina o nível de qualidade desejado (de 0 a 100) definindo a **propriedade \_ \_ VBRQUALITY desejada MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="660a9-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="660a9-128">A taxa de bits baseada em qualidade não codifica o conteúdo para nenhum parâmetro de buffer predefinido.</span><span class="sxs-lookup"><span data-stu-id="660a9-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="660a9-129">Esse nível de qualidade que será mantido para todo o fluxo, independentemente dos requisitos de taxa de bits resultantes.</span><span class="sxs-lookup"><span data-stu-id="660a9-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="660a9-130">Para fluxos de vídeo, defina a taxa média de bits como um valor diferente de zero no atributo de taxa de [**\_ \_ \_ bits média MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia de saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="660a9-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="660a9-131">A taxa de bits precisa é atualizada após a conclusão da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="660a9-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="660a9-132">O exemplo de código a seguir mostra a implementação de setencodingproperties.</span><span class="sxs-lookup"><span data-stu-id="660a9-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="660a9-133">Essa função define as propriedades de codificação de nível de fluxo para CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="660a9-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="660a9-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="660a9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="660a9-135">Tipos de codificação ASF</span><span class="sxs-lookup"><span data-stu-id="660a9-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



