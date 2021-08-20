---
description: Codificação de taxa de bits de variável irr pouco restrita
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codificação de taxa de bits de variável irr pouco restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 986d47e8e518b75e19e578dda30b4bf44b6d2a05a314c20a8d7b988a2016ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057594"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a>Codificação de taxa de bits de variável irr pouco restrita

No modo de codificação VBR (taxa de bits variável) irr pouco restrita, o conteúdo é codificado para a qualidade mais alta possível, mantendo uma taxa de bits especificada.

A codificação VBR irr pouco restrita usa duas passagens de codificação. Ao usar a codificação VBR irr pouco restrita, você especifica uma taxa de bits para o fluxo, como faria com a Codificação de Taxa de Bits [Constante.](constant-bit-rate-encoding.md) No entanto, o codificador usa esse valor apenas como a taxa média de bits para o fluxo e codifica para que a qualidade seja a mais alta possível, mantendo a média. Amostras individuais produzidas pelo codificador variam de tamanho sem limites de buffer explícitos. No entanto, a taxa média de bits durante a sessão de codificação e a duração do fluxo não devem ser mais do que o valor especificado por você. A taxa de bits real em qualquer ponto no fluxo codificado pode variar muito do valor médio. Você não configura uma janela de buffer para codificação VBR irr pouco restrita. Em vez disso, o codificador calcula o tamanho da janela de buffer necessária com base nos requisitos dos exemplos codificados. Isso significa que não há nenhum limite para o tamanho de amostras individuais no fluxo, desde que a taxa média de bits seja menor ou igual ao valor definido.

A vantagem da codificação VBR irr pouco restrita é que o fluxo compactado tem a melhor qualidade possível, mantendo-se dentro de uma largura de banda média previsível. Use isso quando precisar especificar uma largura de banda, mas flutuações em torno da largura de banda especificada são aceitáveis; por exemplo, somente para arquivos locais ou para download.

A desvantagem desse modo de codificação é que o codificador pode definir a janela do buffer como qualquer valor necessário após a codificação, não dando a você controle sobre o tamanho do buffer. Na maioria dos casos, se você não estiver preocupado com o tamanho do buffer ou com a consistência do uso de largura de banda, deverá usar a Codificação de Taxa de Bits variável baseada [em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Configurando o codificador para VBR irr pouco restrito

A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp.h. As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída. Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md). Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída do VBR com suporte e selecionar o necessário no codificador [Media Foundation Transformação](media-foundation-transforms.md) (MFT) com base na taxa média de bits.

A lista a seguir mostra as propriedades que você deve definir para esse tipo de codificação:

-   Especifique o modo de codificação VBR definindo a propriedade \_ MFPKEY VBRENABLED como VARIANT \_ TRUE.
-   De definir o MFPKEY PASSESUSED como 2 porque o modo VBR irr pouco \_ restrito usa duas passagens de codificação.
-   Ao enumerar o tipo de mídia de saída, verifique o atributo [**\_ \_ \_ MF AUDIO AVG \_ BYTES PER \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo [**\_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis. Escolha um tipo de mídia de saída que tenha a taxa de bits média mais próxima da taxa de bits média desejada que você deseja que o codificador mantenha no conteúdo codificado. Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [Negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

Para obter o valor da janela de buffer definido pelo codificador, chame **IWMCodecLeakyBucket::GetBufferSizeBits**, definido em wmcodecifaces.h e wmcodecdspuuid.lib, após a sessão de codificação. Para adicionar suporte irredido à VBR para os fluxos, você deve definir esse valor no atributo [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores médios de bucket com vazamento) no objeto de configuração de fluxo durante a configuração do perfil ASF.

O exemplo a seguir modifica o método SetEncodingType da classe de exemplo CEncoder para configurar o modo VBR irr pouco restrito. Para obter informações sobre essa classe, consulte [Código de exemplo do codificador](encoder-example-code.md). Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte Using the Media Foundation Code Examples.


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

[O modelo de buffer de bucket vazado](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Como criar uma topologia para codificação Two-Pass Windows mídia](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



