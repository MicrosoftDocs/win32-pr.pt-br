---
description: Interfaces Media Foundation
ms.assetid: 3e367190-4c88-430e-adbf-9837e1bf0d2b
title: Interfaces Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12379dc83287b2a03ae0223a5a9a7d945d8fa77
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930101"
---
# <a name="media-foundation-interfaces"></a>Interfaces Media Foundation

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapture"><strong>IAdvancedMediaCapture</strong></a><br/></td>
<td>Habilita a captura de mídia avançada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediacapture/nn-mfmediacapture-iadvancedmediacaptureinitializationsettings"><strong>IAdvancedMediaCaptureInitializationSettings</strong></a><br/></td>
<td>Fornece configurações de inicialização para a captura de mídia avançada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapturesettings"><strong>IAdvancedMediaCaptureSettings</strong></a><br/></td>
<td>Fornece configurações para a captura de mídia avançada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9"><strong>IDirect3DDeviceManager9</strong></a><br/></td>
<td>Permite que dois threads compartilhem o mesmo dispositivo Direct3D 9 e forneça acesso aos recursos de DXVA (DirectX Video Acceleration) do dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice"><strong>IDirectXVideoAccelerationService</strong></a><br/></td>
<td>Fornece serviços de aceleração de vídeo do DirectX (DXVA) de um dispositivo Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder"><strong>IDirectXVideoDecoder</strong></a><br/></td>
<td>Representa um dispositivo de decodificador de vídeo do DirectX Video Acceleration (DXVA).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice"><strong>IDirectXVideoDecoderService</strong></a><br/></td>
<td>Fornece acesso aos serviços de decodificador DXVA (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a><br/></td>
<td>Define o tipo de memória de vídeo para superfícies de vídeo descompactadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor"><strong>IDirectXVideoProcessor</strong></a><br/></td>
<td>Representa um dispositivo de processador de vídeo de aceleração de vídeo do DirectX (DXVA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice"><strong>IDirectXVideoProcessorService</strong></a><br/></td>
<td>Fornece acesso aos serviços de processamento de vídeo DXVA (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a><br/></td>
<td>Define o número de Pins de entrada no filtro EVR ( <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>processador de vídeo avançado</strong></a> do DirectShow).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex"><strong>IEVRFilterConfigEx</strong></a><br/></td>
<td>Configura o filtro EVR ( <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>processador de vídeo avançado</strong></a> do DirectShow).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin"><strong>IEVRTrustedVideoPlugin</strong></a><br/></td>
<td>Permite que um componente de plug-in para o processador de vídeo avançado (EVR) funcione com mídia protegida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a><br/></td>
<td>Não há suporte para essa interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer"><strong>IMF2DBuffer</strong></a><br/></td>
<td>Representa um buffer que contém uma superfície bidimensional, como um quadro de vídeo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2"><strong>IMF2DBuffer2</strong></a><br/></td>
<td>Representa um buffer que contém uma superfície bidimensional, como um quadro de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate"><strong>IMFActivate</strong></a><br/></td>
<td>Permite que o aplicativo adie a criação de um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo"><strong>IMFASFContentInfo</strong></a><br/></td>
<td>Fornece métodos para trabalhar com a seção de cabeçalho de arquivos em conformidade com a especificação ASF (Advanced Systems Format). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer"><strong>IMFASFIndexer</strong></a><br/></td>
<td>Fornece métodos para trabalhar com índices em arquivos ASF (Systems Format).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer"><strong>IMFASFMultiplexer</strong></a><br/></td>
<td>Fornece métodos para criar pacotes de dados ASF (Advanced Systems Format).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion"><strong>IMFASFMutualExclusion</strong></a><br/></td>
<td>Configura um objeto de exclusão mútua ASF (Advanced Systems Format), que gerencia informações sobre um grupo de fluxos em um perfil ASF que são mutuamente exclusivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile"><strong>IMFASFProfile</strong></a><br/></td>
<td>Gerencia um perfil ASF (Advanced Systems Format).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter"><strong>IMFASFSplitter</strong></a><br/></td>
<td>Fornece métodos para ler dados de um arquivo ASF (Advanced Systems Format).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig"><strong>IMFASFStreamConfig</strong></a><br/></td>
<td>Define as configurações de um fluxo em um arquivo ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization"><strong>IMFASFStreamPrioritization</strong></a><br/></td>
<td>Não implementado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector"><strong>IMFASFStreamSelector</strong></a><br/></td>
<td>Seleciona fluxos em um arquivo ASF (Advanced Systems Format), com base nas informações de exclusão mútua no cabeçalho ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback"><strong>IMFAsyncCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para notificar o aplicativo quando um método assíncrono for concluído. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mfobjects/nn-mfobjects-imfasynccallbacklogging"><strong>IMFAsyncCallbackLogging</strong></a><br/></td>
<td>Fornece informações de log sobre o objeto pai ao qual o retorno de chamada assíncrono está associado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a><br/></td>
<td>Fornece informações sobre o resultado de uma operação assíncrona. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a><br/></td>
<td>Fornece uma maneira genérica de armazenar pares de chave/valor em um objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a><br/></td>
<td>O <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a> não está mais disponível para uso a partir do Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy"><strong>IMFAudioPolicy</strong></a><br/></td>
<td>Configura a sessão de áudio associada ao processador de áudio de streaming (SAR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume"><strong>IMFAudioStreamVolume</strong></a><br/></td>
<td>Controla os níveis de volume de canais de áudio individuais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfbufferlistnotify"><strong>IMFBufferListNotify</strong></a><br/></td>
<td>Habilita o objeto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a> a notificar seus clientes sobre alterações de estado importantes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream"><strong>IMFByteStream</strong></a><br/></td>
<td>Representa um fluxo de bytes de alguma fonte de dados, que pode ser um arquivo local, um arquivo de rede ou alguma outra fonte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering"><strong>IMFByteStreamBuffering</strong></a><br/></td>
<td>Controla como um fluxo de bytes armazena em buffer dados de uma rede. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol"><strong>IMFByteStreamCacheControl</strong></a><br/></td>
<td>Controla como um fluxo de bytes de rede transfere dados para um cache local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2"><strong>IMFByteStreamCacheControl2</strong></a><br/></td>
<td>Controla como um fluxo de bytes de rede transfere dados para um cache local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler"><strong>IMFByteStreamHandler</strong></a><br/></td>
<td>Cria uma origem de mídia de um fluxo de bytes. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory"><strong>IMFByteStreamProxyClassFactory</strong></a><br/></td>
<td>Cria um proxy para um fluxo de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek"><strong>IMFByteStreamTimeSeek</strong></a><br/></td>
<td>Busca um fluxo de bytes por posição de tempo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine"><strong>IMFCaptureEngine</strong></a><br/></td>
<td>Controla um ou mais dispositivos de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory"><strong>IMFCaptureEngineClassFactory</strong></a><br/></td>
<td>Cria uma instância do mecanismo de captura.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback"><strong>IMFCaptureEngineOnEventCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para receber eventos do mecanismo de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para receber dados do mecanismo de captura.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2"><strong>IMFCaptureEngineOnSampleCallback2</strong></a><br/></td>
<td>Extensões para a interface de retorno de chamada <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a> que é usada para receber dados do mecanismo de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink"><strong>IMFCapturePhotoSink</strong></a><br/></td>
<td>Controla o coletor de fotos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink"><strong>IMFCapturePreviewSink</strong></a><br/></td>
<td>Controla o coletor de visualização.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink"><strong>IMFCaptureRecordSink</strong></a><br/></td>
<td>Controla o coletor de gravação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a><br/></td>
<td>Controla um coletor de captura, que é um objeto que recebe um ou mais fluxos de um dispositivo de captura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink2"><strong>IMFCaptureSink2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a> para fornecer a funcionalidade de configuração dinâmica do tipo de mídia de saída do coletor de registros ou do coletor de visualização.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource"><strong>IMFCaptureSource</strong></a><br/></td>
<td>Controla o objeto de origem de captura. A fonte de captura gerencia os dispositivos de captura de áudio e vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify"><strong>IMFCdmSuspendNotify</strong></a><br/></td>
<td>Usado para permitir que o cliente notifique o módulo de descriptografia de conteúdo (CDM) quando os recursos globais devem ser colocados em um estado consistente antes da suspensão. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock"><strong>IMFClock</strong></a><br/></td>
<td>Fornece informações de tempo de um relógio no Microsoft Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer"><strong>IMFClockConsumer</strong></a><br/></td>
<td>Implementado por um aplicativo para obter acesso ao <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink"><strong>IMFClockStateSink</strong></a><br/></td>
<td>Recebe notificações de alteração de estado do relógio de apresentação. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection"><strong>IMFCollection</strong></a><br/></td>
<td>Representa uma coleção genérica de ponteiros <strong>IUnknown</strong> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext"><strong>IMFContentDecryptorContext</strong></a><br/></td>
<td>Permite que um descriptografador gerencie chaves de hardware e descriptografe amostras de hardware.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler"><strong>IMFContentEnabler</strong></a><br/></td>
<td>Implementa uma etapa que deve ser executada para que o usuário acesse o conteúdo de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice"><strong>IMFContentProtectionDevice</strong></a><br/></td>
<td>Permite que um descriptografador se comunique com o processador de segurança que implementa a descriptografia de hardware para um sistema de proteção. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager"><strong>IMFContentProtectionManager</strong></a><br/></td>
<td>Permite a reprodução de conteúdo protegido fornecendo ao aplicativo um ponteiro para um objeto de habilitador de conteúdo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample"><strong>IMFDesiredSample</strong></a><br/></td>
<td>Habilita o apresentador para o processador de vídeo avançado (EVR) solicitar um quadro específico do mixer de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit"><strong>IMFDLNASinkInit</strong></a><br/></td>
<td>Inicializa o coletor de mídia de rede de vida digital (DLNA). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper"><strong>IMFDRMNetHelper</strong></a><br/></td>
<td>Configura o Windows Media Digital Rights Management (DRM) para dispositivos de rede em um coletor de rede.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer"><strong>IMFDXGIBuffer</strong></a><br/></td>
<td>Representa um buffer que contém uma superfície de DXGI (infraestrutura gráfica) do Microsoft DirectX.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a><br/></td>
<td>Permite que dois threads compartilhem o mesmo dispositivo Microsoft Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="imfdxgidevicemanagersource.md"><strong>IMFDXGIDeviceManagerSource</strong></a><br/></td>
<td>Fornece a funcionalidade para obter o <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a> do coletor de renderização de vídeo Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock"><strong>IMFFieldOfUseMFTUnlock</strong></a><br/></td>
<td>Permite que um aplicativo use uma Media Foundation transformação (MFT) que tenha restrições em seu uso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink"><strong>IMFFinalizableMediaSink</strong></a><br/></td>
<td>Opcionalmente, com suporte dos coletores de mídia para executar as tarefas necessárias antes do desligamento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a><br/></td>
<td>Consulta um objeto para uma interface de serviço especificada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest"><strong>IMFHttpDownloadRequest</strong></a><br/></td>
<td>Os aplicativos implementam essa interface para substituir a implementação padrão dos protocolos HTTP e HTTPS usados pelo Microsoft Media Foundation. Os aplicativos fornecem a interface <strong>IMFHttpDownloadRequest</strong> para Media Foundation por meio do método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest"><strong>CreateRequest</strong></a> na interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a><br/></td>
<td>Os aplicativos implementam essa interface para substituir a implementação padrão dos protocolos HTTP e HTTPS usados pelo Microsoft Media Foundation. Os aplicativos fornecem a interface <strong>IMFHttpDownloadSession</strong> para Media Foundation por meio do método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> na interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a> . Microsoft Media Foundation usa essa interface para executar um "streaming" ou "progressivo", o download de um recurso identificado por uma URL HTTP ou HTTPS. Várias solicitações HTTP podem ser enviadas para baixar o recurso. A interface <strong>IMFHttpDownloadSession</strong> é usada para criar essas solicitações HTTP individuais.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a><br/></td>
<td>Os aplicativos implementam essa interface para fornecer uma implementação de download HTTP ou HTTPS personalizada. Use a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a> para registrar o provedor. Para obter mais informações, consulte <a href="using-the-source-resolver.md">usando o resolvedor de origem</a>. Depois de registrado, o Microsoft Media Foundation invocará o método <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> da implementação do provedor para abrir URLs http ou HTTPS em vez de usar a implementação padrão.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a><br/></td>
<td>Habilita o compartilhamento de imagens.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory"><strong>IMFImageSharingEngineClassFactory</strong></a><br/></td>
<td>Cria uma instância do <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority"><strong>IMFInputTrustAuthority</strong></a><br/></td>
<td>Permite que outros componentes no caminho de mídia protegido (PMP) usem o sistema de proteção de entrada fornecido por um ITA (autoridades de confiança de entrada).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration"><strong>IMFLocalMFTRegistration</strong></a><br/></td>
<td>Registra Media Foundation transformações (MFTs) no processo do chamador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer"><strong>IMFMediaBuffer</strong></a><br/></td>
<td>Representa um bloco de memória que contém dados de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a><br/></td>
<td>Permite que um aplicativo reproduza arquivos de áudio ou vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a><br/></td>
<td>Cria uma instância do mecanismo de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2"><strong>IMFMediaEngineClassFactory2</strong></a><br/></td>
<td>Cria uma instância do objeto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex"><strong>IMFMediaEngineClassFactoryEx</strong></a><br/></td>
<td>Extensão da interface <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme"><strong>IMFMediaEngineEME</strong></a><br/></td>
<td>Implementado pelo mecanismo de mídia para adicionar métodos de extensões de mídia criptografadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex"><strong>IMFMediaEngineEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension"><strong>IMFMediaEngineExtension</strong></a><br/></td>
<td>Permite que um aplicativo carregue recursos de mídia no mecanismo de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify"><strong>IMFMediaEngineNeedKeyNotify</strong></a><br/></td>
<td>Representa um retorno de chamada para o mecanismo de mídia para notificar os dados de solicitação de chave.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify"><strong>IMFMediaEngineNotify</strong></a><br/></td>
<td>Interface de retorno de chamada para a interface <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo"><strong>IMFMediaEngineOPMInfo</strong></a><br/></td>
<td>Fornece métodos para obter informações sobre o OPM ( <a href="output-protection-manager.md">Gerenciador de proteção de saída</a> ).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent"><strong>IMFMediaEngineProtectedContent</strong></a><br/></td>
<td>Permite que o mecanismo de mídia Reproduza conteúdo de vídeo protegido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a><br/></td>
<td>Fornece ao mecanismo de mídia uma lista de recursos de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex"><strong>IMFMediaEngineSrcElementsEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a> para fornecer recursos adicionais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer"><strong>IMFMediaEngineSupportsSourceTransfer</strong></a><br/></td>
<td>Permite que a origem de mídia seja transferida entre o mecanismo de mídia e o mecanismo de compartilhamento para o Play to.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginewebsupport"><strong>IMFMediaEngineWebSupport</strong></a><br/></td>
<td>Habilita a reprodução de áudio da Web.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror"><strong>IMFMediaError</strong></a><br/></td>
<td>Fornece o status de erro atual para o mecanismo de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent"><strong>IMFMediaEvent</strong></a><br/></td>
<td>Representa um evento gerado por um objeto Media Foundation. Use esta interface para obter informações sobre o evento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a><br/></td>
<td>Recupera eventos de qualquer Media Foundation objeto que gera eventos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue"><strong>IMFMediaEventQueue</strong></a><br/></td>
<td>Fornece uma fila de eventos para aplicativos que precisam implementar a interface <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a><br/></td>
<td>Representa as chaves de mídia usadas para descriptografar dados de mídia usando um sistema de chave de Rights Management digital (DRM). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession"><strong>IMFMediaKeySession</strong></a><br/></td>
<td>Representa uma sessão com o sistema de chave de Rights Management digital (DRM).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysessionnotify"><strong>IMFMediaKeySessionNotify</strong></a><br/></td>
<td>Fornece um mecanismo para notificar o aplicativo sobre informações relacionadas à sessão de chave de mídia. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession"><strong>IMFMediaSession</strong></a><br/></td>
<td>Fornece controles de reprodução para conteúdo protegido e desprotegido.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a><br/></td>
<td>Habilita o compartilhamento de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory"><strong>IMFMediaSharingEngineClassFactory</strong></a><br/></td>
<td>Cria uma instância do <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink"><strong>IMFMediaSink</strong></a><br/></td>
<td>Implementado por objetos de coletor de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll"><strong>IMFMediaSinkPreroll</strong></a><br/></td>
<td>Permite que um coletor de mídia receba amostras antes que o relógio de apresentação seja iniciado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a><br/></td>
<td>Implementado por objetos de origem de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex"><strong>IMFMediaSourceEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> para fornecer recursos adicionais para uma origem de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a><br/></td>
<td>Fornece a funcionalidade para o MSE (extensão de origem de mídia).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextensionnotify"><strong>IMFMediaSourceExtensionNotify</strong></a><br/></td>
<td>Fornece a funcionalidade para gerar eventos associados a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider"><strong>IMFMediaSourcePresentationProvider</strong></a><br/></td>
<td>Fornece notificações para a origem do sequenciador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider"><strong>IMFMediaSourceTopologyProvider</strong></a><br/></td>
<td>Permite que um aplicativo obtenha uma topologia da origem do sequenciador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream"><strong>IMFMediaStream</strong></a><br/></td>
<td>Representa um fluxo em uma fonte de mídia. <br/></td>
</tr>
<tr class="odd">
<td><a href="imfmediastreamsourcesamplerequest.md"><strong>IMFMediaStreamSourceSampleRequest</strong></a><br/></td>
<td>Representa uma solicitação de um exemplo de um MediaStreamSource. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange"><strong>IMFMediaTimeRange</strong></a><br/></td>
<td>Representa uma lista de intervalos de tempo, em que cada intervalo é definido por uma hora de início e de término.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype"><strong>IMFMediaType</strong></a><br/></td>
<td>Representa uma descrição de um formato de mídia. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler"><strong>IMFMediaTypeHandler</strong></a><br/></td>
<td>Obtém e define os tipos de mídia em um objeto, como uma origem de mídia ou um coletor de mídia. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata"><strong>IMFMetadata</strong></a><br/></td>
<td>Gerencia os metadados de um objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a><br/></td>
<td>Obtém metadados de uma fonte de mídia ou outro objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager"><strong>IMFMuxStreamAttributesManager</strong></a><br/></td>
<td>Fornece acesso ao <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a> dos subfluxos de uma fonte de mídia multiplexada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager"><strong>IMFMuxStreamSampleManager</strong></a><br/></td>
<td>Fornece a capacidade de recuperar objetos <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a> para subfluxos individuais dentro da saída de uma fonte de mídia multiplexada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager"><strong>IMFMuxStreamMediaTypeManager</strong></a><br/></td>
<td>Habilita o gerenciamento de configurações de fluxo para uma fonte de mídia multiplexada. Uma configuração de fluxo define um conjunto de subfluxos que podem ser incluídos na saída multiplexada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential"><strong>IMFNetCredential</strong></a><br/></td>
<td>Define e recupera informações de nome de usuário e senha para fins de autenticação. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache"><strong>IMFNetCredentialCache</strong></a><br/></td>
<td>Obtém as credenciais do cache de credenciais.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager"><strong>IMFNetCredentialManager</strong></a><br/></td>
<td>Implementado por aplicativos para fornecer credenciais de usuário para uma fonte de rede.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcrossoriginsupport"><strong>IMFNetCrossOriginSupport</strong></a><br/></td>
<td>Implementado por clientes que desejam impor uma política de origem cruzada para downloads de mídia do HTML5. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator"><strong>IMFNetProxyLocator</strong></a><br/></td>
<td>Determina o proxy a ser usado ao conectar-se a um servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory"><strong>IMFNetProxyLocatorFactory</strong></a><br/></td>
<td>Cria um objeto localizador de proxy, que determina o proxy a ser usado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter"><strong>IMFNetResourceFilter</strong></a><br/></td>
<td>Notifica o aplicativo quando um fluxo de bytes solicita uma URL e permite que o aplicativo bloqueie o redirecionamento de URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig"><strong>IMFNetSchemeHandlerConfig</strong></a><br/></td>
<td>Configura um plug-in de esquema de rede. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream"><strong>IMFObjectReferenceStream</strong></a><br/></td>
<td>Realiza marshaling de um ponteiro de interface de e para um fluxo. <br/> Os objetos de fluxo que dão suporte a <strong>IStream</strong> podem expor essa interface para fornecer marshaling personalizado para ponteiros de interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy"><strong>IMFOutputPolicy</strong></a><br/></td>
<td>Encapsula uma política de uso de uma autoridade de confiança de entrada (ITA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema"><strong>IMFOutputSchema</strong></a><br/></td>
<td>Encapsula informações sobre um sistema de proteção de saída e seus dados de configuração correspondentes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority"><strong>IMFOutputTrustAuthority</strong></a><br/></td>
<td>Encapsula a funcionalidade de um ou mais sistemas de proteção de saída com suporte de uma saída confiável.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol"><strong>IMFPluginControl</strong></a><br/></td>
<td>Controla como as fontes de mídia e as transformações são enumeradas no Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2"><strong>IMFPluginControl2</strong></a><br/></td>
<td>Controla como as fontes de mídia e as transformações são enumeradas no Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem"><strong>IMFPMediaItem</strong></a><br/></td>
<td>Representa um item de mídia. (Preterido.)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a><br/></td>
<td>Contém métodos para reproduzir arquivos de mídia. (Preterido.)<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback"><strong>IMFPMediaPlayerCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para a interface <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient"><strong>IMFPMPClient</strong></a><br/></td>
<td>Permite que uma fonte de mídia receba um ponteiro para a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp"><strong>IMFPMPClientApp</strong></a><br/></td>
<td>Fornece um mecanismo para uma fonte de mídia para implementar a funcionalidade de proteção de conteúdo em aplicativos da Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a><br/></td>
<td>Permite que uma fonte de mídia no processo do aplicativo Crie objetos no processo do caminho de mídia protegido (PMP).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp"><strong>IMFPMPHostApp</strong></a><br/></td>
<td>Permite que uma fonte de mídia crie um objeto de <a href="/windows/desktop/WinRT/reference">Windows Runtime</a> no processo de <a href="protected-media-path.md">caminho de mídia protegido</a> (PMP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver"><strong>IMFPMPServer</strong></a><br/></td>
<td>Permite que duas instâncias da <a href="media-session.md">sessão de mídia</a> compartilhem o mesmo processo PMP (caminho de mídia protegido). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a><br/></td>
<td>Representa um relógio de apresentação, que é usado para agendar quando os exemplos são renderizados e para sincronizar vários fluxos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor"><strong>IMFPresentationDescriptor</strong></a><br/></td>
<td>Descreve os detalhes de uma apresentação. Uma <em>apresentação</em> é um conjunto de fluxos de mídia relacionados que compartilham um tempo de apresentação comum. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource"><strong>IMFPresentationTimeSource</strong></a><br/></td>
<td>Fornece os horários do relógio para o relógio de apresentação. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess"><strong>IMFProtectedEnvironmentAccess</strong></a><br/></td>
<td>Fornece um método que permite que os sistemas de proteção de conteúdo executem um handshake com o ambiente protegido. Isso é necessário porque as APIs <strong>CreateFile</strong> e <strong>DeviceIoControl</strong> não estão disponíveis para aplicativos da Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a><br/></td>
<td>Permite que o Gerenciador de qualidade ajuste a qualidade de áudio ou vídeo de um componente no pipeline.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a><br/></td>
<td>Permite que um objeto de pipeline ajuste sua própria qualidade de áudio ou vídeo, em resposta a mensagens de qualidade.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits"><strong>IMFQualityAdviseLimits</strong></a><br/></td>
<td>Consulta um objeto para o número de <em>modos de qualidade</em> com suporte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager"><strong>IMFQualityManager</strong></a><br/></td>
<td>Ajusta a qualidade da reprodução. Essa interface é exposta pelo Gerenciador de qualidade. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a><br/></td>
<td>Obtém ou define a taxa de reprodução. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a><br/></td>
<td>Consulta o intervalo de taxas de reprodução com suporte, incluindo reprodução reversa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory"><strong>IMFReadWriteClassFactory</strong></a><br/></td>
<td>Cria uma instância do gravador do coletor ou do leitor de origem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a><br/></td>
<td>Notifica um objeto de pipeline para se registrar com o serviço do Agendador de classes de multimídia (MMCSS).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex"><strong>IMFRealTimeClientEx</strong></a><br/></td>
<td>Notifica um objeto de pipeline para se registrar com o serviço do Agendador de classes de multimídia (MMCSS). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfremoteasynccallback"><strong>IMFRemoteAsyncCallback</strong></a><br/></td>
<td>Usado pelo Media Foundation DLL de proxy/stub para realizar marshaling de certas chamadas de método assíncrono entre limites de processo.<br/> Os aplicativos não usam nem implementam essa interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin"><strong>IMFRemoteDesktopPlugin</strong></a><br/></td>
<td>Modifica uma topologia para uso em um ambiente de serviços de terminal. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy"><strong>IMFRemoteProxy</strong></a><br/></td>
<td>Exposto por objetos que atuam como um proxy para um objeto remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle"><strong>IMFSAMIStyle</strong></a><br/></td>
<td>Define e recupera estilos de SAMI (intercâmbio de mídia acessível) sincronizados na <a href="sami-media-source.md">fonte de mídia Sami</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a><br/></td>
<td>Representa um exemplo de mídia, que é um objeto de contêiner para dados de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para obter dados de mídia do coletor de amostra. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2"><strong>IMFSampleGrabberSinkCallback2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream"><strong>IMFSampleOutputStream</strong></a><br/></td>
<td>Grava amostras de mídia em um fluxo de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection"><strong>IMFSampleProtection</strong></a><br/></td>
<td>Fornece criptografia para dados de mídia dentro do caminho de mídia protegido (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob"><strong>IMFSaveJob</strong></a><br/></td>
<td>Persiste dados de mídia de um fluxo de bytes de origem para um fluxo de bytes fornecido pelo aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler"><strong>IMFSchemeHandler</strong></a><br/></td>
<td>Cria uma origem de mídia ou um fluxo de bytes a partir de uma URL. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel"><strong>IMFSecureChannel</strong></a><br/></td>
<td>Estabelece um canal seguro unidirecional entre dois objetos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo"><strong>IMFSeekInfo</strong></a><br/></td>
<td>Para uma posição de busca específica, obtém os dois quadros-chave mais próximos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport"><strong>IMFSensorActivitiesReport</strong></a><br/></td>
<td>Fornece acesso a objetos <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a> que descrevem a atividade atual de um sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback"><strong>IMFSensorActivitiesReportCallback</strong></a><br/></td>
<td>Interface implementada pelo cliente para receber retornos de chamada quando os relatórios de atividade do sensor estiverem disponíveis.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor"><strong>IMFSensorActivityMonitor</strong></a><br/></td>
<td>Fornece métodos para controlar um monitor de atividade de sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a><br/></td>
<td>Representa um relatório de atividade para um sensor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice"><strong>IMFSensorDevice</strong></a><br/></td>
<td>Representa um dispositivo de sensor que pode pertencer a um grupo de sensores, que é representado pela interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a> . O termo &quot; dispositivo &quot; nesse contexto pode se referir a um dispositivo físico, uma fonte de mídia personalizada ou um provedor de quadro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a><br/></td>
<td>Representa um grupo de dispositivos de sensor do qual um <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> pode ser criado. O termo &quot; dispositivo &quot; nesse contexto pode se referir a um dispositivo físico, uma fonte de mídia personalizada ou um provedor de quadro. Um grupo de sensores pode realmente conter vários dispositivos de sensor ou conter apenas um único dispositivo, mas ele ainda se comporta como um grupo de sensores.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity"><strong>IMFSensorProcessActivity</strong></a><br/></td>
<td>Representa a atividade de um processo associado a um sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection"><strong>IMFSensorProfileCollection</strong></a><br/></td>
<td>Contém uma coleção de objetos de perfil de sensor do Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile"><strong>IMFSensorProfile</strong></a><br/></td>
<td>Descreve um perfil de sensor do Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream"><strong>IMFSensorStream</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory"><strong>IMFSensorTransformFactory</strong></a><br/></td>
<td>A interface implementada por transformações de sensor para permitir que o pipeline de mídia consulte os requisitos da transformação do sensor e crie uma instância de tempo de execução da transformação do sensor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource"><strong>IMFSequencerSource</strong></a><br/></td>
<td>Implementado pela <a href="sequencer-source.md">origem do sequenciador</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory"><strong>IMFSharingEngineClassFactory</strong></a><br/></td>
<td>Cria uma instância do mecanismo de compartilhamento de mídia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown"><strong>IMFShutdown</strong></a><br/></td>
<td>Exposto por alguns objetos Media Foundation que devem ser desligados explicitamente. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary"><strong>IMFSignedLibrary</strong></a><br/></td>
<td>Fornece um método que permite que os sistemas de proteção de conteúdo obtenham o endereço de procedimento de uma função na biblioteca assinada. Esse método fornece a mesma funcionalidade que o <strong>GetProcAddress</strong> , que não está disponível para aplicativos da Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume"><strong>IMFSimpleAudioVolume</strong></a><br/></td>
<td>Controla o nível de volume mestre da sessão de áudio associada ao processador de áudio de streaming (SAR) e à fonte de captura de áudio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a><br/></td>
<td>Implementado pelo objeto gravador do coletor de Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para o gravador de coletor de Media Foundation. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2"><strong>IMFSinkWriterCallback2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig"><strong>IMFSinkWriterEncoderConfig</strong></a><br/></td>
<td>Fornece funcionalidade adicional no gravador do coletor para alterar dinamicamente o tipo de mídia e a configuração do codificador. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex"><strong>IMFSinkWriterEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a><br/></td>
<td>Representa um buffer que contém dados de mídia para um <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a><br/></td>
<td>Representa uma coleção de objetos <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify"><strong>IMFSourceBufferNotify</strong></a><br/></td>
<td>Fornece a funcionalidade para gerar eventos associados a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor"><strong>IMFSourceOpenMonitor</strong></a><br/></td>
<td>Interface de retorno de chamada para receber notificações de uma fonte de rede no andamento de uma operação de abertura assíncrona.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a><br/></td>
<td>Implementado pelo objeto leitor de fonte Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a><br/></td>
<td>Interface de retorno de chamada para o leitor de fonte Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2"><strong>IMFSourceReaderCallback2</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex"><strong>IMFSourceReaderEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a><br/></td>
<td>Cria uma fonte de mídia de uma URL ou de um fluxo de bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a><br/></td>
<td>Representa uma seção de dados de áudio com metadados posicionais e de renderização associados. Os objetos de áudio espaciais são armazenados em instâncias <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> e permitem a passagem de informações de áudio espacial entre os componentes Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a><br/></td>
<td>Representa um exemplo de multimídia com informações de som espaciais. Cada <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> contém um ou mais objetos <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager"><strong>IMFSSLCertificateManager</strong></a><br/></td>
<td>Implementado por um cliente e chamado pelo Media Foundation para obter o certificado de protocolo SSL do cliente (SSL) solicitado pelo servidor. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor"><strong>IMFStreamDescriptor</strong></a><br/></td>
<td>Obtém informações sobre um fluxo em uma fonte de mídia. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig"><strong>IMFStreamingSinkConfig</strong></a><br/></td>
<td>Passa informações de configuração para os coletores de mídia que são usados para transmitir o conteúdo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink"><strong>IMFStreamSink</strong></a><br/></td>
<td>Representa um fluxo em um objeto de coletor de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsystemid"><strong>IMFSystemId</strong></a><br/></td>
<td>Fornece um método que retireves os dados de ID do sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate"><strong>IMFTimecodeTranslate</strong></a><br/></td>
<td>Converte entre os códigos de tempo da sociedade de imagem de movimento e dos engenheiros de televisão (SMPTE) e as unidades de hora de 100-nanossegundos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext"><strong>IMFTimedText</strong></a><br/></td>
<td>Um objeto de texto com tempo representa um componente de texto cronometrado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary"><strong>IMFTimedTextBinary</strong></a><br/></td>
<td>Representa o conteúdo de dados de um objeto de texto cronometrado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue"><strong>IMFTimedTextCue</strong></a><br/></td>
<td>Representa o objeto de sinalização de texto cronometrado. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext"><strong>IMFTimedTextFormattedText</strong></a><br/></td>
<td>Representa um bloco de texto com tempo formatado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify"><strong>IMFTimedTextNotify</strong></a><br/></td>
<td>Interface que define retornos de chamada para Media Foundation notificações de texto cronometradas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion"><strong>IMFTimedTextRegion</strong></a><br/></td>
<td>Representa a região de exibição de um objeto de texto com tempo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle"><strong>IMFTimedTextStyle</strong></a><br/></td>
<td>Representa o estilo de texto cronometrado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack"><strong>IMFTimedTextTrack</strong></a><br/></td>
<td>Representa uma faixa de texto cronometrado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist"><strong>IMFTimedTextTrackList</strong></a><br/></td>
<td>Representa uma lista de faixas de texto com tempo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer"><strong>IMFTimer</strong></a><br/></td>
<td>Fornece um temporizador que invoca um retorno de chamada em um horário especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader"><strong>IMFTopoLoader</strong></a><br/></td>
<td>Converte uma topologia parcial em uma topologia completa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology"><strong>IMFTopology</strong></a><br/></td>
<td>Representa uma topologia. Uma <em>topologia</em> descreve uma coleção de fontes de mídia, coletores e transformações que estão conectadas em uma determinada ordem.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode"><strong>IMFTopologyNode</strong></a><br/></td>
<td>Representa um nó em uma topologia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor"><strong>IMFTopologyNodeAttributeEditor</strong></a><br/></td>
<td>Atualiza os atributos de um ou mais nós na topologia atual da sessão de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup"><strong>IMFTopologyServiceLookup</strong></a><br/></td>
<td>Habilita um mixer de vídeo ou apresentador de vídeo personalizado para obter ponteiros de interface do <a href="enhanced-video-renderer.md">processador de vídeo avançado</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient"><strong>IMFTopologyServiceLookupClient</strong></a><br/></td>
<td>Inicializa um mixer de vídeo ou apresentador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample"><strong>IMFTrackedSample</strong></a><br/></td>
<td>Rastreia as contagens de referência em um exemplo de mídia de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile"><strong>IMFTranscodeProfile</strong></a><br/></td>
<td>Implementado pelo objeto de perfil transcodificar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider"><strong>IMFTranscodeSinkInfoProvider</strong></a><br/></td>
<td>Implementado pelo objeto de ativação do coletor transcodificar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a><br/></td>
<td>Implementado por todas as <a href="media-foundation-transforms.md">transformações de Media Foundation</a> (MFTs).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput"><strong>IMFTrustedInput</strong></a><br/></td>
<td>Implementado por componentes que fornecem ITAs (autoridades de confiança de entrada). Essa interface é usada para obter o ITA para cada um dos fluxos do componente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput"><strong>IMFTrustedOutput</strong></a><br/></td>
<td>Implementado por componentes que fornecem OTAs (autoridades de confiança de saída).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid"><strong>IMFVideoDeviceID</strong></a><br/></td>
<td>Retorna o identificador do dispositivo com suporte de um componente de processador de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol"><strong>IMFVideoDisplayControl</strong></a><br/></td>
<td>Controla como o <a href="enhanced-video-renderer.md">processador de vídeo avançado</a> (EVR) exibe vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype"><strong>IMFVideoMediaType</strong></a><br/></td>
<td>Representa uma descrição de um formato de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap"><strong>IMFVideoMixerBitmap</strong></a><br/></td>
<td>Alfa-combina uma imagem de bitmap estática com o vídeo exibido pelo <a href="enhanced-video-renderer.md">processador de vídeo avançado</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol"><strong>IMFVideoMixerControl</strong></a><br/></td>
<td>Controla como o <a href="enhanced-video-renderer.md">processador de vídeo aprimorado</a> (EVR) combina os subfluxos de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2"><strong>IMFVideoMixerControl2</strong></a><br/></td>
<td>Controla as preferências de desentrelaçamento de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a><br/></td>
<td>Mapeia uma posição em um fluxo de vídeo de entrada para a posição correspondente em um fluxo de vídeo de saída.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter"><strong>IMFVideoPresenter</strong></a><br/></td>
<td>Representa um apresentador de vídeo. Um <em>apresentador de vídeo</em> é um objeto que recebe quadros de vídeo, normalmente de um mixer de vídeo, e os apresenta de alguma forma, normalmente, Renderizando-os para a exibição.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor"><strong>IMFVideoProcessor</strong></a><br/></td>
<td>Controla o processamento de vídeo no <a href="enhanced-video-renderer.md">processador de vídeo avançado</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol"><strong>IMFVideoProcessorControl</strong></a><br/></td>
<td>Configura o MFT do <a href="video-processor-mft.md"><strong>processador de vídeo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2"><strong>IMFVideoProcessorControl2</strong></a><br/></td>
<td>Configura o MFT do <a href="video-processor-mft.md"><strong>processador de vídeo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a><br/></td>
<td>Define um novo mixer ou apresentador para o <a href="enhanced-video-renderer.md">processador de vídeo avançado</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator"><strong>IMFVideoSampleAllocator</strong></a><br/></td>
<td>Aloca amostras de vídeo para um coletor de mídia de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a><br/></td>
<td>Permite que um aplicativo acompanhe amostras de vídeo alocadas pelo EVR (processador de vídeo avançado).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex"><strong>IMFVideoSampleAllocatorEx</strong></a><br/></td>
<td>Aloca amostras de vídeo que contêm superfícies de textura do Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify"><strong>IMFVideoSampleAllocatorNotify</strong></a><br/></td>
<td>O retorno de chamada para a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex"><strong>IMFVideoSampleAllocatorNotifyEx</strong></a><br/></td>
<td>O retorno de chamada para a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a><br/></td>
<td>Controla as filas de trabalho criadas pela <a href="media-session.md">sessão de mídia</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex"><strong>IMFWorkQueueServicesEx</strong></a><br/></td>
<td>Estende a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol"><strong>IPlayToControl</strong></a><br/></td>
<td>Permite que o objeto <strong>PlayToConnection</strong> se conecte a um elemento de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrolwithcapabilities"><strong>IPlayToControlWithCapabilities</strong></a><br/></td>
<td>Fornece a funcionalidade para o <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSource</strong></a> para determinar os recursos do conteúdo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSourceClassFactory</strong></a><br/></td>
<td>Cria uma instância do objeto <a href="/uwp/api/Windows.Media.PlayTo.PlayToSource"><strong>PlayToSource</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket"><strong>IWMCodecLeakyBucket</strong></a><br/></td>
<td>Configura os parâmetros de &quot; Bucket vazados &quot; em um codificador de vídeo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp"><strong>IWMCodecOutputTimestamp</strong></a><br/></td>
<td>Obtém o carimbo de data/hora do próximo quadro de vídeo a ser decodificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata"><strong>IWMCodecPrivateData</strong></a><br/></td>
<td>Obtém os dados do codec privado que devem ser acrescentados ao tipo de mídia de saída. Esses dados de codec são necessários para decodificar corretamente o conteúdo de vídeo do Windows Media.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops"><strong>IWMCodecProps</strong></a><br/></td>
<td>Fornece métodos que recuperam Propriedades de codec específicas de formato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings"><strong>IWMCodecStrings</strong></a><br/></td>
<td>Recupera nomes e cadeias de caracteres descritivas para codecs e formatos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops"><strong>IWMColorConvProps</strong></a><br/></td>
<td>Define propriedades no DSP do conversor de cores. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops"><strong>IWMResamplerProps</strong></a><br/></td>
<td>Define propriedades no DSP do reamostrador de áudio. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops"><strong>IWMResizerProps</strong></a><br/></td>
<td>Define propriedades no DSP do redimensionador de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport"><strong>IWMSampleExtensionSupport</strong></a><br/></td>
<td>Configura o suporte de codec para extensões de exemplo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup"><strong>IWMVideoDecoderHurryup</strong></a><br/></td>
<td>Controla a velocidade do decodificador de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer"><strong>IWMVideoDecoderReconBuffer</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta interface está obsoleta e não deve ser usada.
</blockquote>
<br/> Gerencia quadros de vídeo reconstruídos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe"><strong>IWMVideoForceKeyFrame</strong></a><br/></td>
<td>Força o codificador a codificar o quadro atual como um quadro-chave. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
