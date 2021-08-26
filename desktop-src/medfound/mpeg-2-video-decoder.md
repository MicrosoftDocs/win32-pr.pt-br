---
description: O Decodificador de Vídeo MPEG-2 é uma Media Foundation que decodifica o vídeo MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e2b270cadb114875fb63bc6c57ce2ddd63eecb2815b8fe3bcee175710d1771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012586"
---
# <a name="mpeg-2-video-decoder"></a>Decodificador de vídeo MPEG-2

O Decodificador de Vídeo MPEG-2 é uma [Media Foundation](media-foundation-transforms.md) que decodifica o vídeo MPEG-1 e MPEG-2. O decodificador dá suporte ao vídeo de perfil MpEG-2 Simple e Main (H.262, ISO/IEC 13818-2) e vídeo MPEG-1 (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipos de entrada

O decodificador dá suporte aos seguintes tipos de mídia de entrada.

| Atributo                                                 | Descrição                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | **Vídeo MFMediaType \_**                                                  |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes tipos de saída.

| Atributo                                                 | Descrição                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | **Vídeo MFMediaType \_**                                                                                                                                                         |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Comentários

O decodificador de vídeo MPEG-2 expõe as seguintes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

A entrada para o decodificador deve ser um fluxo elementar. A resolução máxima com suporte é de 1920 × 1088 pixels.

O decodificador dá suporte à DXVA (Aceleração de Vídeo DirectX) usando o Microsoft Direct3D 9 ou o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modos especiais de decodificação

-   **Modo de baixa latência.** Esse modo é apropriado para cenários como comunicações em tempo real. Ele reduz a latência de início, portanto, o decodificador produz a primeira amostra de saída mais cedo. No entanto, o decodificador em buffers menos amostras nesse modo, o que pode potencialmente levar a falhas, porque o decodificador não decodifica tantos quadros com antecedência. Para habilitar o modo de baixa latência, de definir o [atributo \_ CODECAPI AVLowLatencyMode.](codecapi-avlowlatencymode.md)
-   **Procurando.** Para busca precisa, chame o [**método IMFTransform::SetOutputBounds.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) Quando esse método é chamado, o decodificador só recebe quadros que se enquadram no intervalo de carimbos de data/hora especificado pelo chamador.
-   **Modo de geração de miniaturas**. Esse modo destina-se à geração rápida de imagens em miniatura. Nesse modo, o decodificador inicialmente decodifica apenas quadros I. Se nenhum quadro I for encontrado em um determinado número de quadros, o decodificador iniciará a decodificação de quadros P e saídas de quadros não I em um intervalo fixo (uma por *N* imagens) até que um quadro I seja atingido. Para habilitar o modo de geração de miniaturas, de definir [a propriedade \_ CODECAPI AVDecVideoThumbnailGenerationMode.](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   **Jogo complicado.** O decodificador pode decodificar em taxas mais rápido do que em tempo real. Com taxas de reprodução mais altas, o decodificador alterna para decodificar apenas quadros I. Para reprodução inversa, somente os quadros I são decodificados.

### <a name="codec-properties"></a>Propriedades do Codec

O decodificador dá suporte às seguintes propriedades por meio do [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| Propriedade                                                                                                      | Descrição                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Habilita ou desabilita o modo de geração de miniaturas.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Habilita ou desabilita a decodificação acelerada de hardware.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita ou desabilita o modo de baixa latência.                                                                      |
| [O \_ DECODIFICADOR MFT \_ EXPÕE TIPOS DE SAÍDA EM ORDEM \_ \_ \_ \_ \_ NATIVA](mft-decoder-expose-output-types-in-native-order.md) | Especifica se o decodificador expõe tipos de saída adequados para transcodificação antes de outros formatos. |



 

Dessas propriedades, o seguinte também pode ser definido por meio da interface [**ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitações

-   Não há suporte para o decodificador em plataformas baseadas em IA-64.
-   O decodificador não dá suporte à descriptografia CSS nem à reprodução de DVDs criptografados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 
