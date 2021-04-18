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
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Codificação de taxa de bits de variável Peak-Constrained

Na taxa de bits variável com restrição de pico (VBR), o conteúdo é codificado para uma taxa de bits especificada e *valores de pico*: uma taxa de bits de pico e uma janela de buffer de pico. Esses valores de pico também são chamados de *valores de Bucket de pico de vazamento*. O arquivo é codificado para estar em conformidade com um buffer descrito pelos valores de pico, de modo que a taxa de bits média geral do fluxo seja igual ou menor que o valor médio de taxa de bits especificado.

Normalmente, a taxa de bits de pico é muito alta. O codificador garante que o valor de taxa de bits médio especificado seja mantido durante a duração do fluxo (taxa média de bits >= (tamanho total do fluxo em bits/duração do fluxo em segundos)). Considere o exemplo a seguir: Configure um fluxo com uma taxa média de bits de 16.000 bits por segundo, uma taxa de bits de pico de 48.000 bits por segundo e uma janela de buffer de pico de 3.000 (3 segundos). O tamanho do buffer usado para o fluxo é de 144.000 bits (48.000 bits por segundo \* 3 segundos) conforme determinado pelos valores de pico. O codificador compacta os dados para que estejam em conformidade com esse buffer. Além disso, a taxa média de bits do fluxo deve ser de 16.000 ou menos. Se o codificador precisar criar amostras grandes para lidar com um segmento de conteúdo complexo, ele poderá aproveitar o tamanho do buffer grande. Mas outras partes do fluxo devem ser codificadas em uma taxa de bits inferior para reduzir a média para o nível especificado. A codificação de taxa de bits de pico restrita é útil para dispositivos de reprodução com uma capacidade de buffer finita e restrições de taxa de dados. Um exemplo comum disso é a codificação usada para DVDs quando a decodificação é executada por um chip em um dispositivo, onde há limitações de hardware que devem ser consideradas.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configurando o codificador para Peak-Constrained VBR

A VBR com restrição de pico é como uma [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) não restrita, pois ela é confinada a uma taxa média de bits durante a duração do fluxo. Além disso, a taxa de bits com restrição de pico está em conformidade com um buffer de pico. Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico. Esse modo usa duas passagens de codificação e fornece a flexibilidade do codificador em como ele codifica exemplos individuais enquanto obedece às limitações de pico.

A configuração do codificador é definida por meio de valores de propriedade. Essas propriedades são definidas em wmcodecdsp. h. As propriedades de configuração devem ser definidas no codificador antes de negociar o tipo de mídia de saída. Para obter informações sobre como definir propriedades no codificador, consulte [Configurando o codificador](configuring-the-encoder.md). Com base nos valores de propriedade especificados, você pode enumerar os tipos de saída de VBR com suporte e selecionar o necessário no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT) com base na taxa média de bits.

Você deve definir o seguinte propertiesfor deste tipo de codificação:

-   Especifique o modo de codificação de VBR definindo a \_ Propriedade MFPKEY VBRENABLED como Variant \_ true.
-   Defina MFPKEY \_ PASSESUSED como 2 porque o modo VBR com restrição de pico usa duas passagens de codificação.
-   Defina MFPKEY \_ RMAX para especificar a taxa de bits de pico e defina MFPKEY \_ BMAX para especificar a janela de pico do buffer.
-   Ao enumerar o tipo de mídia de saída, verifique o atributo de [**\_ média de \_ \_ \_ bytes \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de [**\_ \_ \_ taxa de bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo) dos tipos de mídia de saída disponíveis e escolha um tipo de mídia de saída que tenha a taxa de bits média mais próxima da taxa de bits média desejada que você deseja que Para obter mais informações sobre como selecionar o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> É recomendável que você defina a taxa de bits de pico para pelo menos duas vezes a taxa média de bits. Definir a taxa de pico para um valor mais baixo pode fazer com que o codificador Codifique o conteúdo como CBR de duas passagens em vez da taxa de bits de pico restrita.

 

Para obter o valor da janela de buffer definido pelo codificador, chame **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido em wmcodecifaces. h, wmcodecdspuuid. lib, após a sessão de codificação. Para adicionar suporte de VBR não restringido para os fluxos, você deve definir esse valor no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (pico de vazamentos de Bucket) no objeto de configuração de fluxo ao configurar o perfil ASF.

O exemplo de código a seguir modifica o método setencodingtype da classe de exemplo CEncoder para configurar o modo de taxa de bits restrita de pico. Para obter informações sobre essa classe, consulte [código de exemplo do codificador](encoder-example-code.md). Para obter informações sobre as macros auxiliares usadas neste exemplo, consulte usando os exemplos de código de Media Foundation.


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

[O modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Como criar uma topologia para Two-Pass a codificação de mídia do Windows](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



