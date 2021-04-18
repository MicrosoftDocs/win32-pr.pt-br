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
# <a name="quality-based-variable-bit-rate-encoding"></a>Codificação de taxa de bits de variável Quality-Based

Ao contrário da constante CBR ( [codificação de taxa de bits](constant-bit-rate-encoding.md) ), em que o codificador se esforça para manter uma taxa de bits específica da mídia codificada, no modo de taxa de bits variável (VBR), o codificador se esforça para obter a melhor qualidade possível da mídia codificada. A principal diferença entre CBR e VBR é o tamanho da janela de buffer usada. Fluxos de taxa de bits codificados geralmente têm janelas de buffer grandes em comparação com os fluxos codificados em CBR.

A qualidade do conteúdo codificado é determinada pela quantidade de dados que é perdida quando o conteúdo é compactado. Muitos fatores afetam a perda de dados no processo de compactação; Mas, em geral, quanto mais complexos os dados originais e maior a taxa de compactação, mais detalhes serão perdidos no processo de compactação.

No modo VBR com base em qualidade, você não define uma taxa de bits ou uma janela de buffer que o codificador deve seguir. Em vez disso, você especifica um nível de qualidade para um fluxo de mídia digital em vez de uma taxa de bits. O codificador compacta o conteúdo para que todos os exemplos sejam de qualidade comparável; Isso garante que a qualidade seja consistente durante toda a duração da reprodução, independentemente dos requisitos de buffer do fluxo resultante.

A codificação VBR baseada em qualidade tende a criar grandes fluxos compactados. Em geral, esse tipo de codificação é adequado para reprodução local ou conexões de rede de largura de banda alta (ou download e reprodução). Por exemplo, você pode escrever um aplicativo para copiar músicas de CD para arquivos ASF em um computador. O uso da codificação VBR com base na qualidade garantiria que todas as músicas copiadas tenham a mesma qualidade. Nesses casos, a qualidade consistente oferecerá uma melhor experiência do usuário.

A desvantagem da codificação de VBR baseada em qualidade é que não há realmente nenhuma maneira de saber os requisitos de tamanho ou largura de banda da mídia codificada antes da sessão de codificação, pois o codificador usa uma única passagem de codificação. Isso pode tornar arquivos codificados em taxa de bits com base em qualidade inadequados para circunstâncias em que a memória ou a largura de banda são restritas, como a reprodução de conteúdo em players de mídia portáteis ou streaming por uma rede de baixa largura de banda

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Configurando o codificador para Quality-Based codificação de VBR

A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp. h. As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída. Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md).

A lista a seguir mostra as propriedades que você deve definir para esse tipo de codificação:

-   Especifique o modo de codificação de VBR definindo a propriedade **MFPKEY \_ VBRENABLED** como Variant \_ true.
-   Defina **MFPKEY \_ PASSESUSED** como 1 porque esse modo VBR usa uma passagem de codificação.
-   Defina o nível de qualidade desejado (de 0 a 100) definindo a **propriedade \_ \_ VBRQUALITY desejada MFPKEY** . A taxa de bits baseada em qualidade não codifica o conteúdo para nenhum parâmetro de buffer predefinido. Esse nível de qualidade que será mantido para todo o fluxo, independentemente dos requisitos de taxa de bits resultantes.
-   Para fluxos de vídeo, defina a taxa média de bits como um valor diferente de zero no atributo de taxa de [**\_ \_ \_ bits média MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia de saída do codificador. A taxa de bits precisa é atualizada após a conclusão da sessão de codificação.

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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de codificação ASF](asf-encoding-types.md)
</dt> </dl>

 

 



