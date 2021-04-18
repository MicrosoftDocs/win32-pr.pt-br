---
description: O decodificador de vídeo MPEG-2 é uma Media Foundation transformação que decodifica o vídeo MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502272"
---
# <a name="mpeg-2-video-decoder"></a>Decodificador de vídeo MPEG-2

O decodificador de vídeo MPEG-2 é uma [Media Foundation transformação](media-foundation-transforms.md) que decodifica o vídeo MPEG-1 e MPEG-2. O decodificador dá suporte ao vídeo de perfil principal e simples MPEG-2 (H. 262, ISO/IEC 13818-2) e vídeo MPEG-1 (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipos de entrada

O decodificador dá suporte aos seguintes tipos de mídia de entrada.

| Atributo                                                 | Descrição                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo do MFMediaType \_**                                                  |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes tipos de saída.

| Atributo                                                 | Descrição                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo do MFMediaType \_**                                                                                                                                                         |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

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

O decodificador dá suporte a DXVA (DirectX Video Acceleration) usando o Microsoft Direct3D 9 ou o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modos de decodificação especiais

-   **Modo de baixa latência.** Esse modo é apropriado para cenários como comunicações em tempo real. Ele reduz a latência de inicialização, portanto, o decodificador produz o primeiro exemplo de saída mais cedo. No entanto, o decodificador armazena em buffer menos amostras nesse modo, o que pode levar a falhas, pois o decodificador não decodifica o máximo de quadros com antecedência. Para habilitar o modo de baixa latência, defina o atributo [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .
-   **Atingir.** Para busca precisa, chame o método [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) . Quando esse método é chamado, o decodificador gera apenas quadros que se enquadram no intervalo de carimbos de data/hora especificado pelo chamador.
-   **Modo de geração de miniatura**. Esse modo destina-se à geração rápida de imagens em miniatura. Nesse modo, o decodificador inicialmente decodifica apenas quadros I. Se nenhum quadro I for encontrado em um determinado número de quadros, o decodificador iniciará a decodificação de quadros P e produzirá quadros não-I em um intervalo fixo (um por *N* imagens) até que um quadro I seja atingido. Para habilitar o modo de geração de miniatura, defina a propriedade [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .
-   **Rodada de toque.** O decodificador pode decodificar taxas com mais rapidez do que o tempo real. Em taxas de reprodução mais altas, o decodificador mudará para decodificar apenas quadros I. Para reprodução reversa, apenas os quadros I são decodificados.

### <a name="codec-properties"></a>Propriedades do codec

O decodificador dá suporte às seguintes propriedades por meio do método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .



| Propriedade                                                                                                      | Descrição                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Habilita ou desabilita o modo de geração de miniatura.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Habilita ou desabilita a decodificação acelerada de hardware.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita ou desabilita o modo de baixa latência.                                                                      |
| [o \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída na \_ \_ ordem nativa](mft-decoder-expose-output-types-in-native-order.md) | Especifica se o decodificador expõe os tipos de saída que são adequados para transcodificação antes de outros formatos. |



 

Dessas propriedades, o seguinte também pode ser definido por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitações

-   Não há suporte para o decodificador em plataformas baseadas em IA-64.
-   O decodificador não dá suporte à descriptografia de CSS nem à reprodução de DVDs criptografados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
