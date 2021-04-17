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
# <a name="unconstrained-variable-bit-rate-encoding"></a>Codificação de taxa de bits variável irrestrita

No modo de codificação de taxa de bits variável (VBR) irrestrito, o conteúdo é codificado para a melhor qualidade possível, mantendo uma taxa de bits especificada.

A codificação de VBR não restringida usa duas passagens de codificação. Ao usar a codificação VBR não restringida, você especifica uma taxa de bits para o fluxo, como faria com a [codificação de taxa de bits constante](constant-bit-rate-encoding.md). No entanto, o codificador usa esse valor somente como a taxa de bits média para o fluxo e codifica para que a qualidade seja a mais alta possível, mantendo a média. Exemplos individuais produzidos pelo codificador variam em tamanho sem nenhum limite de buffer explícito. No entanto, a taxa de bits média durante a sessão de codificação e a duração do fluxo não devem ser mais do que o valor especificado por você. A taxa de bits real em qualquer ponto no fluxo codificado pode variar muito do valor médio. Você não define uma janela de buffer para a codificação de VBR não restringida. Em vez disso, o codificador computa o tamanho da janela de buffer necessária com base nos requisitos dos exemplos codificados. Isso significa que não há nenhum limite para o tamanho de amostras individuais no fluxo, desde que a taxa de bits média seja menor ou igual ao valor definido.

A vantagem da codificação de VBR não restringida é que o fluxo compactado tem a melhor qualidade possível enquanto permanece dentro de uma largura de banda média previsível. Use isso quando precisar especificar uma largura de banda, mas flutuações em relação à largura de banda especificada são aceitáveis; por exemplo, para arquivos locais ou somente para download.

A desvantagem desse modo de codificação é que o codificador pode definir a janela de buffer para qualquer valor necessário após a codificação, dando-lhe nenhum controle sobre o tamanho do buffer. Na maioria dos casos, se você não estiver preocupado com o tamanho do buffer ou a consistência do uso da largura de banda, use a [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Configurando o codificador para uma VBR não restringida

A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp. h. As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída. Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md). Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída de VBR com suporte e selecionar o necessário no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT) com base na taxa média de bits.

A lista a seguir mostra as propriedades que você deve definir para esse tipo de codificação:

-   Especifique o modo de codificação de VBR definindo a \_ Propriedade MFPKEY VBRENABLED como Variant \_ true.
-   Defina MFPKEY \_ PASSESUSED como 2 porque o modo VBR não restringido usa duas passagens de codificação.
-   Ao enumerar o tipo de mídia de saída, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de taxa de [**\_ \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis. Escolha um tipo de mídia de saída que tenha a taxa de bits média mais próxima da taxa de bits média desejada que você deseja que o codificador mantenha no conteúdo codificado. Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

Para obter o valor da janela buffer é definido pelo codificador, chame **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido em wmcodecifaces. h e wmcodecdspuuid. lib, após a sessão de codificação. Para adicionar suporte de VBR não restringido para os fluxos, você deve definir esse valor no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores de Bucket de perda média) no objeto de configuração de fluxo ao configurar o perfil ASF.

O seguinte modifica o método setencodingtype da classe de exemplo CEncoder para configurar o modo VBR não restringido. Para obter informações sobre essa classe, consulte [código de exemplo do codificador](encoder-example-code.md). Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte usando os exemplos de código de Media Foundation.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de codificação ASF](asf-encoding-types.md)
</dt> <dt>

[O modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Como criar uma topologia para Two-Pass a codificação de mídia do Windows](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



