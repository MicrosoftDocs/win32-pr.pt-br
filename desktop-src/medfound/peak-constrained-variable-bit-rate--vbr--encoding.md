---
description: 'Na VBR (taxa de bits de variável restrita de pico), o conteúdo é codificado em uma taxa de bits e valores de pico especificados: uma taxa de bits de pico e uma janela de buffer de pico.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained codificação de taxa de bits variável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97361c6d4ac8cefd33b223157347e450252691cab024e167862f50c7aac0fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737663"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained codificação de taxa de bits variável

Na VBR (taxa de bits de variável restrita de pico), o conteúdo é codificado em uma taxa de bits e valores de pico especificados: uma taxa de bits de pico e uma janela de buffer de pico. Esses valores de pico também são chamados de *valores de bucket com vazamento de pico.* O arquivo é codificado para estar em conformidade com um buffer descrito pelos valores de pico, de modo que a taxa de bits média geral do fluxo seja igual ou menor que o valor médio da taxa de bits especificado.

Normalmente, a taxa de bits de pico é bastante alta. O codificador garante que o valor médio da taxa de bits especificado seja mantido durante a duração do fluxo (taxa média de bits >= (tamanho total do fluxo em bits/duração do fluxo em segundos)). Considere o exemplo a seguir: configure um fluxo com uma taxa média de bits de 16.000 bits por segundo, uma taxa de bits de pico de 48.000 bits por segundo e uma janela de buffer de pico de 3.000 (3 segundos). O tamanho do buffer usado para o fluxo é de 144.000 bits (48.000 bits por segundo 3 segundos), conforme determinado pelos valores de \* pico. O codificador compacta os dados para estar em conformidade com esse buffer. Além disso, a taxa média de bits do fluxo deve ser de 16.000 ou menos. Se o codificador deve criar amostras grandes para lidar com um segmento complexo de conteúdo, ele pode aproveitar o tamanho do buffer grande. Mas outras partes do fluxo devem ser codificadas a uma taxa de bits inferior para reduzir a média para o nível especificado. A codificação VBR com restrição de pico é útil para dispositivos de reprodução com uma capacidade de buffer finita e restrições de taxa de dados. Um exemplo comum disso é a codificação usada para DVDs quando a decodificação é executada por um chip em um dispositivo, em que há limitações de hardware que devem ser consideradas.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configurando o codificador para Peak-Constrained VBR

A VBR com restrição de pico é como uma [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) irredida, já que ela é limitada a uma taxa média de bits durante a duração do fluxo. Além disso, o VBR com restrição de pico está em conformidade com um buffer de pico. Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico. Esse modo usa duas passagens de codificação e fornece a flexibilidade do codificador em como codifica amostras individuais enquanto adere às limitações de pico.

A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp.h. As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída. Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md). Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída VBR com suporte e selecionar o necessário na MFT [(transformação](media-foundation-transforms.md) Media Foundation codificador) com base na taxa média de bits.

Você deve definir as seguintes propriedadespara esse tipo de codificação:

-   Especifique o modo de codificação VBR definindo a propriedade \_ MFPKEY VBRENABLED como VARIANT \_ TRUE.
-   De definir o MFPKEY PASSESUSED como 2 porque o modo VBR com restrição de pico \_ usa duas passagens de codificação.
-   De configurar MFPKEY RMAX para especificar a taxa de bits de pico e \_ definir MFPKEY \_ BMAX para especificar a janela de buffer de pico.
-   Ao enumerar o tipo de mídia de saída, verifique o atributo [**\_ \_ \_ MF MT AUDIO AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo [**\_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis e escolha um tipo de mídia de saída que tenha a taxa média de bits mais próxima da taxa de bits média desejada que você deseja que o codificador mantenha no conteúdo codificado. Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [Negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> É recomendável definir a taxa de bits de pico como pelo menos duas vezes a taxa média de bits. Definir a taxa de pico como um valor mais baixo pode fazer com que o codificador codificar o conteúdo como CBR de duas passs em vez de VBR com restrição de pico.

 

Para obter o valor da janela de buffer definido pelo codificador, chame **IWMCodecLeakyBucket::GetBufferSizeBits**, definido em wmcodecifaces.h, wmcodecdspuuid.lib, após a sessão de codificação. Para adicionar suporte irr pouco restrito à VBR para os fluxos, você deve definir esse valor no atributo [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valores de bucket com vazamento de pico) no objeto de configuração de fluxo ao configurar o perfil ASF.

O exemplo de código a seguir modifica o método SetEncodingType da classe de exemplo CEncoder para configurar o modo VBR com restrição de pico. Para obter informações sobre essa classe, consulte [Código de exemplo do codificador](encoder-example-code.md). Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte Using the Media Foundation Code Examples.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de codificação ASF](asf-encoding-types.md)
</dt> <dt>

[O modelo de buffer de bucket vazado](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Como criar uma topologia para codificação Two-Pass Windows mídia](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



