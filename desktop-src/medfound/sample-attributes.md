---
description: Atributos de exemplo
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Atributos de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56593978a411b314e6e988c031ee36869c4ea44212fd7f154e3ba18478400b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776976"
---
# <a name="sample-attributes"></a>Atributos de exemplo

Os atributos a seguir se aplicam [a Exemplos de Mídia](media-samples.md). Para obter os atributos de um exemplo de mídia, use a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| Atributo                                                                                                      | Descrição                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Especifica se um exemplo de mídia contém um quadro de vídeo 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Especifica a predominância de campo para um quadro de vídeo entrelaçado.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | A explicação da câmera para o exemplo.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | O [**armazenamento IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para todos os metadados relacionados ao pipeline de captura.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indica se um exemplo de vídeo é um quadro-chave.                                                                                                                                                                                                   |
| [KeyID de conteúdo MFSampleExtension \_ \_](mfsampleextension-content-keyid.md)                                       | Define a ID da chave para o exemplo.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Especifica se um quadro de vídeo desintercalado foi derivado do campo superior ou do campo inferior.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | O carimbo de data/hora do driver do dispositivo.                                                                                                                                                                                                             |
| [**Descontinuidade de MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md)                          | Especifica se um exemplo de mídia é o primeiro exemplo após uma lacuna no fluxo.                                                                                                                                                                    |
| [Criptografia MFSampleExtension \_ \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Especifica o tamanho do bloco de byte criptografado para criptografia de padrão baseada em exemplo.                                                                                                                                                                       |
| [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Especifica o esquema de proteção para exemplos criptografados.                                                                                                                                                                                             |
| [MFSampleExtension \_ Encryption \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Especifica a ID de um exemplo criptografado.                                                                                                                                                                                                           |
| [SkipByteBlock de criptografia MFSampleExtension \_ \_](mfsampleextension-encryption-skipbyteblock.md)                 | Especifica o tamanho do bloco de byte claro (não criptografado) para criptografia de padrão baseada em exemplo.                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Define o mapeamento de sub amostra para o exemplo que indica os bytes limpos e criptografados nos dados de exemplo.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Especifica se um quadro de vídeo está corrompido.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Obtém um objeto do tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contém objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contêm naLUs (unidades de camada de abstração de rede) e unidades SEI (Informações de Aprimoramento Suplementar) encaminhadas por um decodificador. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Especifica o tipo, NALU ou SEI, de uma unidade anexada a [**um IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) em uma coleção [MFSampleExtension \_ ForwardedDecodeUnits.](mfsampleextension-forwardeddecodeunits.md)                                                    |
| [**MFSampleExtension \_ Entrelaçado**](mfsampleextension-interlaced-attribute.md)                                | Indica se um quadro de vídeo é entrelaçado ou progressivo.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Especifica informações de quadro LTR (Referência de Longo Prazo) e é retornado no exemplo de saída.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Esse atributo retorna a diferença absoluta média (MAD) em todos os blocos de macro no plano Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Especifica os limites de carga para um quadro. Isso se aplica a exemplos criptografados.                                                                                                                                                                   |
| [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)                                      | Contém a miniatura da foto de [**um IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contém o [**IMFMediaType que**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) descreve o tipo de formato de imagem contido no atributo [MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | Os intrínsecos da câmera de pino para o exemplo.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado.                                                                                                                                                                                |
| [ROIRectangle de MFSampleExtension \_](mfsampleextension-roirectangle.md)                                          | Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | O valor em Nits que especifica a luminância de luz de fundo global direcionada para o quadro de vídeo associado.                                                                                                                                           |
| [**MFSampleExtension \_ Token**](mfsampleextension-token-attribute.md)                                          | Contém um ponteiro para o token que foi fornecido para o [**método IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Especifica o QP (parâmetro de quantização) que foi usado para codificar um exemplo de vídeo.                                                                                                                                                                  |



 

Nem todos os exemplos de mídia contêm todos os atributos listados aqui. Em alguns casos, um atributo se aplica somente a determinados tipos de dados. Por exemplo, alguns atributos se aplicam somente a exemplos de vídeo e não devem aparecer em amostras de áudio. Em outros casos, o atributo tem um valor padrão que se aplica se o atributo não estiver definido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> </dl>

 

 



