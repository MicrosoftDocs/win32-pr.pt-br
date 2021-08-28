---
description: Descreve APIs de vídeo equivalentes do Direct3D 12 para versões anteriores.
ms.assetid: ''
title: Migração para o vídeo do Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 4004c35c21d9d6c67c0af3f9413521cf845437cddbc2ce245c3da495ed3daca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777416"
---
# <a name="migrating-to-direct3d-12-video"></a>Migração para o vídeo do Direct3D 12

Este artigo descreve as APIs de vídeo do Direct3D 12 que são usadas para implementar recursos disponíveis em versões anteriores. Para melhorar o desempenho e a usabilidade dos recursos de vídeo de prioridade mais alta, alguns recursos do Direct3D 11 não têm suporte total ou parcial no Direct3D 12. 

Observe que, embora a maioria dos recursos do Direct3D 11 está disponível no Direct3D 12, o design da API foi alterado, portanto, em muitos casos, não há um mapeamento um para um das APIs entre os dois conjuntos de API. As tabelas a seguir destinam-se a apontar para as APIs mais relevantes no Direct3D 12 para cada API do Direct3D 11, mas a maneira como você usa as novas APIs pode ser significativamente diferente. Por exemplo:

- Para decodificar um quadro de vídeo, as APIs de vídeo do Direct3D 11 usam chamadas para [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe), [GetDecoderBuffer,](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)e [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). Com o Direct3D 12, um único método é usado,  [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe).
- Para processamento de vídeo, o Direct3D 11 forneceu métodos individuais para definir os vários valores de configuração, como [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) e [VideoProcessorSetOutputAlphaFillMode.](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) No Direct3D 12, esses valores são definidos quando o processador de vídeo é criado, na chamada para [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)ou quando o quadro é processado com uma chamada para [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1).





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Fornece a funcionalidade de vídeo de um dispositivo Direct3D 11, incluindo decodificação de vídeo, processamento de vídeo, proteção de conteúdo baseada em GPU e criptografia/descriptografia de vídeo. Essa funcionalidade é parcialmente implementada para o Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [ConfigureAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Não implementado |
| [DecoderBeginFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList::D ecodeFrame,](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe)  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT,](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument) [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM,](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream) [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [DecoderEndFrame](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [DecoderExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Não implementado. |
| [DecryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Não implementado. |
| [EncryptionBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Não implementado. |
| [FinishSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Não implementado. |
| [GetDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Não implementado. Buffers compactados são gerenciados pelo aplicativo no Direct3D 12. |
| [GetEncryptionBltKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Não implementado. | 
| [NegotiateAuthenticatedChannelKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Não implementado. |
| [NegotiateCryptoSessionKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Não implementado. |
| [QueryAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Não implementado. |
| [ReleaseDecoderBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Não implementado. Buffers compactados são gerenciados pelo aplicativo no Direct3D 12. |
| [StartSessionKeyRefresh](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Não implementado |
| [SubmitDecoderBuffers](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorBlt](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [VideoProcessorGetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [VideoProcessorSetOutputAlphaFillMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. AlphaFillMode](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [VideoProcessorSetOutputBackgroundColor](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Backgroundcolor](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [VideoProcessorSetOutputColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [VideoProcessorGetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [VideoProcessorSetOutputConstriction](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) | Não implementado. Não há suporte para DRM de software. |
| [VideoProcessorGetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [VideoProcessorSetOutputExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) | Não implementado. |
| [VideoProcessorGetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [VideoProcessorSetOutputStereoMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. EnableStereo](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [VideoProcessorSetOutputTargetRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. TargetRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [VideoProcessorGetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [VideoProcessorSetStreamAlpha](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha)  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Alfa](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [VideoProcessorGetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [VideoProcessorSetStreamAutoProcessingMode](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. EnableAutoProcessing](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [VideoProcessorSetStreamColorSpace](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [VideoProcessorSetStreamDestRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. DestinationRectangle](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [VideoProcessorSetStreamExtension](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) | Não implementado. |
| [VideoProcessorGetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [VideoProcessorSetStreamFilter](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. FilterFlags](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [VideoProcessorSetStreamFrameFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Formato](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [VideoProcessorSetStreamLumaKey](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. LumaKey](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [VideoProcessorSetStreamOutputRate](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Framerate](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [VideoProcessorSetStreamPalette](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) | Não implementado |
| [VideoProcessorGetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [VideoProcessorSetStreamPixelAspectRatio](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Transformar](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [VideoProcessorSetStreamRotation](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Transformar](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [VideoProcessorSetStreamSourceRect](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Transformar](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [VideoProcessorGetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [VideoProcessorSetStreamStereoFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Transformar](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Fornece funcionalidade de vídeo estendida de um dispositivo Direct3D 11, incluindo DRM de hardware, melhorias de uso da superfície, mais funcionalidade de processamento de vídeo. Essa funcionalidade é implementada para o Direct3D 12 por meio de novas interfaces.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| CheckCryptoSessionStatus | TBD | 
| [DecoderEnableDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [DecoderUpdateDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [GetDataForNewHardwareKey](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | TBD |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList::D ecodeFrame](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [VideoProcessorGetBehaviorHints](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | TBD |
| [VideoProcessorGetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [VideoProcessorGetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [VideoProcessorSetOutputShaderUsage](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) | TBD |
| [VideoProcessorGetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. Colorspace](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [VideoProcessorGetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [VideoProcessorSetStreamMirror](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Transformar](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Representa um decodificador de vídeo acelerado por hardware para Direct3D 11. Essa é uma interface de wrapper em [torno de ID3D11VideoContext](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) que expõe a funcionalidade de decodificação real. Não há nenhuma API equivalente para vídeo do Direct3D 12.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Identifica as superfícies de saída que podem ser acessadas durante a decodificação de vídeo. No Direct3D 12, a interface [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) usa [objetos ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) diretamente.

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Fornece os recursos de processamento de vídeo e de decodificação de vídeo de um dispositivo Direct3D 11. Esse é o ponto de entrada principal para criar o dispositivo de decodificador de vídeo e a sessão de criptografia e para processamento de vídeo, funcionalidades, perfis etc. Essa funcionalidade é parcialmente implementada para o Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckCryptoKeyExchange](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Não implementado. |
| [CheckVideoDecoderFormat](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [CreateAuthenticatedChannel](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Não implementado. |
| [CreateCryptoSession](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Não implementado. |
| [CreateVideoDecoder](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice::CreateVideoDecoder](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [CreateVideoDecoderOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessor](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice::CreateVideoProcessor](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| [CreateVideoProcessorEnumerator](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | N/D |
| [CreateVideoProcessorInputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [CreateVideoProcessorOutputView](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [GetContentProtectionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | TBD
| [GetVideoDecoderConfig](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | Somente o modo VLD tem suporte no Direct3D 12. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [GetVideoDecoderConfigCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | N/D |
| [GetVideoDecoderProfile](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [GetVideoDecoderProfileCount](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. ProfileCount](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object::SetPrivateDataInterface](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Fornece recursos estendidos de processamento de vídeo e de decodificação de vídeo de um dispositivo Direct3D 11, incluindo mais extensões, DRM de hardware, downsampling de decodificação, recursos do decodificador de vídeo etc. Essa funcionalidade é implementada para o Direct3D 12.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [CheckVideoDecoderDownsampling](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [GetCryptoSessionPrivateDataSize](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | TBD |
| [GetVideoDecoderCaps](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [RecommendVideoDecoderDownsampleParameters](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Representa um processador de vídeo para Direct3D 11. Essa funcionalidade é implementada para Direct3D 12 no [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor)

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [GetContentDesc](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Não implementado |
| [GetRateConversionCaps](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Não implementado |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator e ID3D11VideoProcessorEnumerator1

Enumera as funcionalidades do processador de vídeo de um dispositivo Direct3D 11.
No Direct3D 12, a funcionalidade de enumeração é substituída por [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport). 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Identifica as superfícies de entrada que podem ser acessadas durante o processamento de vídeo.
No Direct3D 12, isso é substituído por ID3D12Texture2D.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Identifica as superfícies de saída que podem ser acessadas durante o processamento de vídeo.
No Direct3D 12, isso é substituído por ID3D12Texture2D.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Fornece um canal de comunicação seguro com o driver de gráficos ou o runtime do Microsoft Direct3D. Essa funcionalidade não é implementada para vídeo do Direct3D 12.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Representa uma sessão criptográfica. Usado para cenários de DRM de software e hardware. Não há nenhuma API pública equivalente para o vídeo do Direct3D 12.

## <a name="related-topics"></a>Tópicos relacionados

[APIs de vídeo do Direct3D 12](direct3d-12-video-apis.md)


 

 




