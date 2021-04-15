---
description: O decodificador de vídeo Media Foundation H. 265 é uma transformação Media Foundation que dá suporte à decodificação de conteúdo H. 265/HEVC no formato anexo B e pode ser usado na reprodução de arquivos MP4 e M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Decodificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502204"
---
# <a name="h265--hevc-video-decoder"></a>Decodificador de vídeo H. 265/HEVC

O decodificador de vídeo Media Foundation H. 265 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à decodificação de conteúdo H. 265/HEVC no formato anexo B e pode ser usado na reprodução de arquivos MP4 e M2TS.

O decodificador de vídeo H. 265 expõe as interfaces a seguir.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (com suporte no Windows 8)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para criar uma instância do decodificador, chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="input-types"></a>Tipos de entrada

O tipo de entrada deve conter pelo menos os dois atributos a seguir:



| Atributo                                                 | Descrição                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo do MFMediaType \_**                                                                        |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ HEVC](video-subtype-guids.md) ou MFVideoFormat \_ HEVC \_ es |



 

O primeiro subtipo de mídia, MFVideoFormat \_ HEVC, indica que os exemplos de mídia carregam H. 265 fragmentado com códigos de início e o fluxo tem SPS/PPS intercalados. Ele assume um quadro por amostra.

O subtipo de mídia MFVideoFormat \_ HEVC \_ es é para indicar os exemplos de mídia que carregam o Element H. 265 fragmentado, em que cada exemplo pode conter uma imagem parcial, várias imagens, algumas imagens e uma imagem parcial.

Os tipos de mídia de entrada não podem ser alterados dinamicamente entre dois tipos. O decodificador pode detectar alterações de formato de saída em andamento com base na sintaxe de fluxo elementar (taxa de proporção, dimensão, sinalizadores de entrelaçamento, informações de colorimetry) e disparar alterações de tipo de mídia de saída correspondente.

Para o tipo de mídia de entrada, o decodificador espera que a origem defina o perfil correto. Por exemplo, se o conteúdo for descompactado, o tipo de mídia de entrada deverá especificar o perfil como Main10.

## <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes subtipos de saída:

-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ P010**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Atributos de transformação

O decodificador H. 265 implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.



| Atributo                                                                                       | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | Habilita ou desabilita o modo de decodificação de baixa latência.                                                                                |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | Define o número de threads de trabalho usados pelo decodificador.                                                                        |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita ou desabilita o modo de geração de miniatura.                                                                                |
| [\_conjunto de \_ tamanhos de NALU MF \_](mf-nalu-length-set.md)                                                 | Indica que as informações de comprimento de NALU serão enviadas como um BLOB com cada exemplo de H. 265 compactada.                              |
| [\_informações de \_ comprimento de NALU MF \_](mf-nalu-length-information.md)                                 | Indica os comprimentos de NALUs no exemplo. Este é um BLOB MF que é definido em exemplos de entrada compactados para o decodificador H. 265. |
| [\_contagem de \_ \_ amostra de saída mínima \_ \_ de e/o de MF](mf-sa-minimum-output-sample-count.md)                 | Especifica o número máximo de amostras de saída.                                                                               |



 

O decodificador H. 265 dá suporte à interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Essa interface fornece uma API alternativate para definir as propriedades de codec a seguir.

-   [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Restrições de formato

O decodificador dá suporte aos seguintes formatos:



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfis/níveis    | Perfis principal, principal ainda e Main10                                                                                                                                                                                                                        |
| Formatos de croma     | 4:2:0 croma                                                                                                                                                                                                                                                         |
| Resolução mínima | 48 × 48 pixels                                                                                                                                                                                                                                                       |
| Resolução máxima | 4096 × 2304 pixels<br/> A resolução máxima garantida para a aceleração de DXVA é 1920 × 1088 pixels; em resoluções mais altas, a decodificação é feita com o DXVA, se for compatível com o hardware subjacente, caso contrário, a decodificação será feita com o software.<br/> |
| DXVA               | O decodificador dá suporte a DX11 e DX12 DXVA, mas não a DXVA versão 2 ou a DXVA versão 1.                                                                                                                                                                                                         |



 

Os dados de entrada devem estar em conformidade com o anexo B do ITU-T H. 265 \| ISO/IEC 23008-2. Os dados devem incluir os códigos de início. O decodificador ignora os bytes até encontrar um conjunto de parâmetros de sequência (SPS) e um conjunto de parâmetros de imagem (PPS) válidos no fluxo de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
