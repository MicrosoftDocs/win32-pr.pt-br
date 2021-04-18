---
description: O decodificador de vídeo Media Foundation H. 264 é uma transformação Media Foundation que dá suporte à decodificação de perfis de linha de base, principal e alto, até o nível 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Decodificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457208"
---
# <a name="h264-video-decoder"></a>Decodificador de vídeo H. 264

O decodificador de vídeo Media Foundation H. 264 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à decodificação de perfis de linha de base, principal e alto, até o nível 5,1.

O decodificador de vídeo H. 264 expõe as interfaces a seguir.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (com suporte no Windows 8)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para criar uma instância do decodificador, siga um destes procedimentos:

-   Chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). O CLSID para o decodificador é **CLSID \_ CMSH264DecoderMFT**, declarado em wmcodecdsp. h.

## <a name="input-types"></a>Tipos de entrada

O tipo de entrada deve conter pelo menos os dois atributos a seguir:



| Atributo                                                 | Descrição                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo do MFMediaType \_**                                                                        |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ H264](video-subtype-guids.md) ou MFVideoFormat de \_ H264 \_ es |



 

Se o tipo de entrada contiver apenas esses dois atributos, o decodificador oferecerá um tipo de saída padrão, que funciona como um espaço reservado. Quando o decodificador recebe amostras de entrada suficientes para produzir um quadro de saída, ele sinaliza uma alteração de formato retornando a **\_ alteração de fluxo MF E \_ Transform \_ \_** de [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Consulte a documentação do **ProcessOutput** para obter detalhes sobre como lidar com alterações de formato.

Para evitar uma alteração de formato inicial, forneça o máximo possível de informações no tipo de entrada, incluindo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Taxa de quadros.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Dimensões do quadro.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modo de entrelaçamento.
<blockquote>
[!Note]<br />
No vídeo H. 264, a estrutura entrelaçada pode ser alterada dinamicamente, portanto, o valor recomendado desse atributo é <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>. As informações de entrelaçamento na transmissão elementar do vídeo têm precedência sobre o tipo de mídia. Para obter mais informações, consulte <a href="video-interlacing.md">vídeo entrelaçado</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Taxa de proporção de pixel.</td>
</tr>
</tbody>
</table>



 

O tipo de entrada deve ser definido antes do tipo de saída. Até que o tipo de entrada seja definido, o método [**IMFTransform:: Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) do codificador retorna **MF \_ E \_ Transform \_ Type \_ não \_ definido**.

## <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes subtipos de saída:

-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Atributos de transformação

O decodificador H. 264 implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.



| Atributo                                                                                       | Descrição                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | Habilita ou desabilita a aceleração de hardware.                                                 |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita ou desabilita o modo de geração de miniatura.                                             |
| [\_Reconhecimento de \_ D3D \_ SA do MF](mf-sa-d3d-aware-attribute.md)                                             | Indica que o decodificador dá suporte a DXVA (aceleração de vídeo do DirectX). Tratar como somente leitura. |



 

No Windows 8, o decodificador H. 264 também oferece suporte aos seguintes atributos.



| Atributo                                                                                                     | Descrição                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita ou desabilita o modo de decodificação de baixa latência.                                                              |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | Define o número de threads de trabalho usados pelo decodificador.                                                      |
| [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Define a largura máxima da imagem que o decodificador aceitará como um tipo de entrada.                               |
| [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | Define a altura máxima da imagem que o decodificador aceitará como um tipo de entrada.                              |
| [\_contagem de \_ \_ amostra de saída mínima \_ \_ de e/o de MF](mf-sa-minimum-output-sample-count.md)                               | Especifica o número máximo de amostras de saída.                                                             |
| [o \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída na \_ \_ ordem nativa](mft-decoder-expose-output-types-in-native-order.md) | Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos. |



 

No Windows 8, o decodificador H. 264 dá suporte à interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Essa interface fornece uma API alternativate para definir as propriedades de codec a seguir.

-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Restrições de formato

O decodificador dá suporte aos seguintes formatos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Perfis/níveis</td>
<td>Perfis de linha de base, principal e alto, até o nível 5,1. (Consulte Especificação ITU-T H. 264 para obter detalhes.)</td>
</tr>
<tr class="even">
<td>Formatos de croma</td>
<td>4:2:0 croma ou monocromático</td>
</tr>
<tr class="odd">
<td>Resolução mínima</td>
<td>48 × 48 pixels</td>
</tr>
<tr class="even">
<td>Resolução máxima</td>
<td>4096 × 2304 pixels<br/> A resolução máxima garantida para a aceleração de DXVA é 1920 × 1088 pixels; em resoluções mais altas, a decodificação é feita com o DXVA, se for compatível com o hardware subjacente, caso contrário, a decodificação será feita com o software.<br/>
<blockquote>
[!Note]<br />
No Windows 7, a resolução máxima com suporte é de 1920 × 1088 pixels para decodificação de software e DXVA.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>O decodificador oferece suporte a DXVA versão 2, mas não a DXVA versão 1. A decodificação de DXVA tem suporte apenas para fragmentado de linha de base, principal e de perfil alto compatíveis com o principal. (Fragmentado de linha de base compatíveis principal são definidos como <strong>profile_idc</strong>= 66 e <strong>constrained_set1_flag</strong>= 1.)</td>
</tr>
</tbody>
</table>



 

Os dados de entrada devem estar em conformidade com o anexo B do ISO/IEC 14496-10. Os dados devem incluir os códigos de início. O decodificador ignora os bytes até encontrar um conjunto de parâmetros de sequência (SPS) e um conjunto de parâmetros de imagem (PPS) válidos no fluxo de bytes.

O decodificador não oferece suporte à tecnologia de refinamento de filmes.

> [!Note]  
> Uma versão anterior da documentação incorretamente afirmou que o decodificador tem suporte no Windows Server 2008 R2.

 

Se o suplemento de atualização de plataforma para Windows Vista estiver instalado, o decodificador de vídeo H. 264 estará disponível no Windows Vista, mas poderá ser acessado somente no Windows Vista usando o [leitor de origem](source-reader.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 
