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
# <a name="constant-bit-rate-encoding"></a>Codificação de taxa de bits constante

Em codificação de taxa de bits constante (CBR), o codificador sabe a taxa de bits dos exemplos de mídia de saída e a janela de buffer (parâmetros de Bucket de vazamento) antes do início da sessão de codificação. O codificador usa o mesmo número de bits para codificar cada segundo de amostra durante a duração do arquivo para atingir a taxa de bits de destino para um fluxo. Isso limita a variação no tamanho dos exemplos de fluxo. Além disso, durante a sessão de codificação, a taxa de bits não está exatamente no valor especificado, mas permanece próxima da taxa de bits de destino.

A codificação CBR é útil quando você quer saber a taxa de bits ou a duração aproximada de um arquivo sem analisar o arquivo inteiro. Isso é necessário em cenários de streaming ao vivo, em que o conteúdo de mídia precisa ser transmitido a uma taxa de bits previsível e com o uso de banda larga consistente.

A desvantagem da codificação CBR é que a qualidade do conteúdo codificado não será constante. Como algum conteúdo é mais difícil de ser compactado, partes de um fluxo de CBR serão de menor qualidade do que outras. Por exemplo, um filme típico tem algumas cenas que são razoavelmente estáticas e algumas cenas que estão cheias de ação. Se você codificar um filme usando CBR, os bastidores que são estáticos e, portanto, fáceis de codificar com eficiência, serão de maior qualidade do que as cenas de ação, o que exigiria tamanhos de amostra mais altos para manter a mesma qualidade.

Em geral, as variações na qualidade de um arquivo CBR são mais pronunciadas em taxas de bits inferiores. Em taxas de bits mais altas, a qualidade de um arquivo codificado em CBR ainda variará, mas os problemas de qualidade serão menos perceptíveis para o usuário. Ao usar a codificação de CBR, você deve definir a largura de banda tão alta quanto o cenário de entrega permitir.

-   [Parâmetros de configuração da CBR](#cbr-configuration-settings)
-   [Configurações de Bucket de vazamento](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Parâmetros de configuração da CBR

Você deve configurar um codificador especificando o tipo de codificação e as várias configurações específicas de fluxo antes da sessão de codificação.

**Para configurar o codificador para a codificação CBR**

1.  Especifique o modo de codificação de CBR.

    Por padrão, o codificador está configurado para usar a codificação CBR. A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp. h. Você pode especificar esse modo explicitamente definindo a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como Variant \_ false. Para obter informações sobre como definir propriedades em codificadores, consulte [Configurando o codificador](configuring-the-encoder.md).

2.  Escolha a taxa de bits de codificação.

    Para a codificação de CBR, você deve saber a taxa de bits na qual deseja codificar o fluxo antes do início da sessão de codificação. Você deve definir a taxa de bits durante enquanto estiver configurando o codificador. Para fazer isso, enquanto você estiver executando a negociação de tipo de mídia, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de [**\_ \_ \_ taxa de bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis e escolha um tipo de mídia de saída que tenha a taxa média de bits mais próxima da taxa de bit de Para obter mais informações, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

O exemplo de código a seguir mostra a implementação de setencodingproperties. Essa função define as propriedades de codificação de nível de fluxo para CBR e VBR.


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



### <a name="leaky-bucket-settings"></a>Configurações de Bucket de vazamento

Para a codificação de CBR, a média e o máximo de valores de Bucket de vazamento para o fluxo são os mesmos. Para obter mais informações sobre esses parâmetros, consulte [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md).

Para codificar os fluxos de áudio de CBR, você precisa definir os valores de Bucket de vazamento depois de negociar o tipo de mídia de saída no codificador. O codificador calcula a janela de buffer internamente com base na taxa média de bits definida no tipo de mídia de saída.

Para definir valores de Bucket de vazamento, crie uma matriz de DWORDs pode definir os valores a seguir na propriedade [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK corrigida MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) no repositório de propriedades do coletor de mídia. Para obter mais informações, consulte [definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).

-   Taxa média de bits: Obtenha a taxa média de bits do tipo de mídia de saída selecionado durante a negociação do tipo de mídia. Use o atributo de [**\_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .
-   Janela buffer: consulte o codificador para a interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e, em seguida, chame [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).
-   Tamanho do buffer inicial: Defina como 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de codificação ASF](asf-encoding-types.md)
</dt> <dt>

[Tutorial: 1-transmitir codificação de mídia do Windows](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: gravando um arquivo WMA usando a codificação de CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
