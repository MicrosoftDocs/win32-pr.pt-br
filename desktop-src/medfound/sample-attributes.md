---
description: Atributos de exemplo
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Atributos de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502252"
---
# <a name="sample-attributes"></a>Atributos de exemplo

Os atributos a seguir se aplicam a [exemplos de mídia](media-samples.md). Para obter os atributos de um exemplo de mídia, use a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Atributo                                                                                                      | Descrição                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Especifica se um exemplo de mídia contém um quadro de vídeo 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Especifica o campo predominância para um quadro de vídeo entrelaçado.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | A câmera é extrínsecos para o exemplo.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | O repositório [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para todos os metadados relacionados ao pipeline de captura.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indica se um exemplo de vídeo é um quadro-chave.                                                                                                                                                                                                   |
| [\_Keyid conteúdo do MFSampleExtension \_](mfsampleextension-content-keyid.md)                                       | Define a ID da chave para o exemplo.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Especifica se um quadro de vídeo desentrelaçado foi derivado do campo superior ou do campo inferior.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | O carimbo de data/hora do driver de dispositivo.                                                                                                                                                                                                             |
| [**Descontinuidade de MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md)                          | Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.                                                                                                                                                                    |
| [MFSampleExtension de \_ criptografia \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Especifica o tamanho do bloco de bytes criptografados para a criptografia de padrão baseada em exemplo.                                                                                                                                                                       |
| [MFSampleExtension de \_ criptografia \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Especifica o esquema de proteção para exemplos criptografados.                                                                                                                                                                                             |
| [\_Exemplo de criptografia MFSampleExtension \_](mfsampleextension-encryption-sampleid.md)                           | Especifica a ID de um exemplo criptografado.                                                                                                                                                                                                           |
| [MFSampleExtension de \_ criptografia \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Especifica o tamanho do bloco de bytes claro (não criptografado) para criptografia de padrão baseada em exemplo.                                                                                                                                                           |
| [MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Define o mapeamento de sub-amostra para o exemplo que indica os bytes claros e criptografados nos dados de exemplo.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Especifica se um quadro de vídeo está corrompido.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Obtém um objeto do tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contém objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contêm NALUs (unidades de camada de abstração de rede) e unidades sei (informações de aprimoramento complementar) encaminhadas por um decodificador. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Especifica o tipo, NALU ou SEI, de uma unidade anexada a um [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) em uma coleção [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) .                                                    |
| [**MFSampleExtension \_ entrelaçado**](mfsampleextension-interlaced-attribute.md)                                | Indica se um quadro de vídeo é entrelaçado ou progressivo.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Esse atributo retorna a diferença absoluta média (MAD) em todos os blocos de macro no plano Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Especifica os limites de carga para um quadro. Isso se aplica a amostras criptografadas.                                                                                                                                                                   |
| [MFSampleExtension \_ Fotominiatura](mfsampleextension-photothumbnail.md)                                      | Contém a miniatura da foto de um [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contém o [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que descreve o tipo de formato de imagem contido no atributo [ \_ keythumbnail MFSampleExtension](mfsampleextension-photothumbnail.md) .                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | A câmera pinhole é intrínseca para o exemplo.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.                                                                                                                            |
| [**MFSampleExtension \_ único**](mfsampleextension-singlefield-attribute.md)                              | Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | O valor em nits que especifica a luminância de luz global de destino para o quadro de vídeo associado.                                                                                                                                           |
| [**\_Token MFSampleExtension**](mfsampleextension-token-attribute.md)                                          | Contém um ponteiro para o token que foi fornecido ao método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Especifica o parâmetro de quantificação (QP) que foi usado para codificar uma amostra de vídeo.                                                                                                                                                                  |



 

Nem todo exemplo de mídia contém todos os atributos listados aqui. Em alguns casos, um atributo se aplica somente a determinados tipos de dados. Por exemplo, alguns atributos se aplicam apenas a amostras de vídeo e não devem aparecer em amostras de áudio. Em outros casos, o atributo tem um valor padrão que se aplica se o atributo não estiver definido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> </dl>

 

 



