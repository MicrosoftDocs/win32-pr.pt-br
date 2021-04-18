---
description: Este tópico descreve como dar suporte ao Microsoft Direct3D 11 em um decodificador Microsoft Media Foundation.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542f7244922dc7947f22e4d33027fdcac1962fe5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105755922"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation

Este tópico descreve como dar suporte ao Microsoft Direct3D 11 em um decodificador Microsoft Media Foundation. Especificamente, ele descreve a comunicação entre o decodificador e o processador de vídeo. Este tópico não descreve como implementar as operações de decodificação.

-   [Visão geral](#overview)
-   [Abrir um identificador de dispositivo](#open-a-device-handle)
-   [Localizar uma configuração de decodificador](#find-a-decoder-configuration)
-   [Fallback para decodificação de software](#fallback-to-software-decoding)
-   [Alocando buffers descompactados](#allocating-uncompressed-buffers)
-   [Decodificação](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

No restante deste tópico, são usados os seguintes termos:

-   **Decodificador de software**. O decodificador de software é a Media Foundation transformação (MFT) que recebe amostras de vídeo compactadas e gera quadros de vídeo descompactados.
-   **Dispositivo decodificador**. O dispositivo decodificador é o acelerador de vídeo e é implementado pelo driver de gráficos. O dispositivo decodificador executa operações de decodificação aceleradas.
-   **Pipeline**. O pipeline hospeda o decodificador de software e entrega buffers de e para o decodificador de software. Dependendo do aplicativo, o pipeline pode ser a sessão de [mídia](media-session.md), o [leitor de origem](source-reader.md)ou o código do aplicativo que chama diretamente o MFT.

Para executar a decodificação usando o Direct3D 11, o decodificador de software deve ter um ponteiro para um dispositivo Direct3D 11. O dispositivo Direct3D 11 é criado externamente ao decodificador de software. Em um cenário de [sessão de mídia](media-session.md) , o processador de vídeo cria o dispositivo Direct3D 11. Em um cenário de [leitor de origem](source-reader.md) , normalmente o aplicativo cria o dispositivo Direct3D 11.

O Gerenciador de Dispositivos DXGI é usado para compartilhar o Direct3D 11 entre componentes. O Gerenciador de Dispositivos DXGI expõe a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . O pipeline define o ponteiro **IMFDXGIDeviceManager** no decodificador de software enviando a mensagem [**MFT do Gerenciador de mensagens do conjunto de valores do \_ \_ \_ D3D \_**](mft-message-set-d3d-manager.md) .

O diagrama a seguir mostra a relação entre o decodificador de software, o Direct3D 11 e o pipeline.

![um diagrama que mostra o decodificador de software e o Gerenciador de dispositivos dxgi.](images/d3d11video01.png)

Aqui estão as etapas básicas que um decodificador de software deve executar para dar suporte ao Direct3D 11 em Media Foundation:

1.  Abra um identificador para o dispositivo Direct3D 11.
2.  Encontre uma configuração de decodificador.
3.  Aloque buffers descompactados.
4.  Decodificar quadros.

Essas etapas são descritas mais detalhadamente no restante deste tópico.

## <a name="open-a-device-handle"></a>Abrir um identificador de dispositivo

O MFT do decodificador usa o Gerenciador de dispositivos DXGI para obter um identificador para o dispositivo Direct3D 11. Para abrir o identificador do dispositivo, execute as seguintes etapas:

1.  O MFT do decodificador deve expor o atributo [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) com o valor **true**.
2.  O carregador de topologia consulta esse atributo chamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). O valor **true** indica que o MFT dá suporte ao Direct3D 11.
3.  O carregador de topologia chama [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**MFT do conjunto de mensagens do \_ \_ \_ \_ Gerenciador de D3D**](mft-message-set-d3d-manager.md) . O parâmetro *ulParam* é um ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para o Gerenciador de dispositivos dxgi. Consulte este ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Chame [**IMFDXGIDeviceManager:: OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) para obter um identificador para o dispositivo Direct3D 11.
5.  Para obter um ponteiro para o dispositivo do Direct3D 11, chame [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Passe o identificador do dispositivo e o valor **IID \_ ID3D11Device**. O método retorna um ponteiro para a interface [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .
6.  Para obter um ponteiro para o acelerador de vídeo, chame [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) novamente. Desta vez, passe o identificador do dispositivo e o valor **IID \_ ID3D11VideoDevice**. O método retorna um ponteiro para a interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
7.  Chame [**ID3D11Device:: GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) para obter um ponteiro [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) .
8.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) para obter um ponteiro [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) .
9.  É recomendável que você use a proteção de vários threads no contexto do dispositivo para evitar problemas de deadlock que às vezes pode acontecer quando você chama [**ID3D11VideoContext:: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) ou [**ID3D11VideoContext:: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Para definir a proteção de vários threads, primeiro chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) para obter um ponteiro [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) . Em seguida, chame [**ID3D10Multithread:: SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), passando **true** para *bMTProtect*.

## <a name="find-a-decoder-configuration"></a>Localizar uma configuração de decodificador

Para executar a decodificação, o decodificador de software deve encontrar uma configuração compatível com suporte do dispositivo decodificador, incluindo um formato de destino de renderização. Essa etapa ocorre dentro do método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , como a seguir.

1.  Valide o tipo de mídia de entrada. Se o tipo for rejeitado, ignore as etapas restantes e retorne um código de erro.
2.  Chame [**ID3D11VideoDevice:: GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) para obter o número de perfis com suporte.
3.  Chame [**ID3D11VideoDevice:: GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) para enumerar os perfis e obter os GUIDs de perfil.
4.  Procure um GUID de perfil que corresponda ao formato de vídeo e aos recursos do decodificador de software. Por exemplo, um decodificador MPEG-2 procura o perfil de decodificador **D3D11 \_ \_ \_ MPEG2 \_ MOCOMP**,**perfil de \_ decodificador do D3D11 \_ \_ MPEG2 \_ IDCT** e **D3D11 de perfil do \_ decodificador \_ \_ MPEG2 \_ VLD**.
5.  Se um GUID de decodificador adequado for encontrado, verifique o formato de saída chamando o método [**ID3D11VideoDevice:: CheckVideoDecoderFormat**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) . Passe o GUID do decodificador e um valor de **\_ formato dxgi** que especifica o formato de destino de renderização.
6.  Em seguida, encontre uma configuração adequada para o decodificador.
    1.  Chame [**ID3D11VideoDevice:: GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) para obter o número de configurações de decodificador. Passe o mesmo GUID do dispositivo decodificador, junto com uma estrutura [**\_ \_ \_ desc de decodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) que descreve o formato de destino render proposto.
    2.  Chame [**ID3D11VideoDevice:: GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) para enumerar as configurações do decodificador.

No método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , retorne um formato de vídeo descompactado com base no formato de destino render proposto.

No método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , verifique o tipo de mídia em relação ao formato de destino de renderização.

## <a name="fallback-to-software-decoding"></a>Fallback para decodificação de software

O MFT pode não conseguir localizar uma configuração. Por exemplo, o driver de gráficos pode não oferecer suporte aos recursos corretos. Nesse caso, o MFT deve retornar à decodificação de software, da seguinte maneira.

1.  Os métodos [**setparâmetrosdeentrada**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) e [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) devem retornar **MF \_ e \_ sem suporte \_ \_ tipo D3D**.
2.  Em resposta, o carregador de topologia enviará a mensagem do Gerenciador de D3D do conjunto de  mensagens de [**MFT \_ \_ \_ \_**](mft-message-set-d3d-manager.md) com o valor NULL para o parâmetro *ulParam* .
3.  O MFT libera seu ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  O carregador de topologia renegocia o tipo de mídia.

Neste ponto, o MFT pode usar a decodificação de software.

## <a name="allocating-uncompressed-buffers"></a>Alocando buffers descompactados

O decodificador é responsável por alocar texturas do Direct3D 11 para usar como buffers de vídeo não compactados. O [atributo \_ \_ contagem de \_ \_ exemplo \_ de saída mínima de MF](mf-sa-minimum-output-sample-count.md) de e/ou no fluxo de saída atributos (consulte [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) é usado para determinar quantas superfícies o decodificador deve alocar para o processador de vídeo usar para desentrelaçamento. Um decodificador deve usar esse valor delimitadondo-o para alguns limites superiores e inferiores razoáveis, por exemplo, 3-32. Para conteúdo progressivo, consulte a [contagem de amostra de saída mínima de MF de \_ \_ \_ entrada \_ \_ \_ progressiva](mf-sa-minimum-output-sample-count-progressive.md).

No método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , defina o **fluxo de saída do MFT fornece um sinalizador de \_ \_ \_ \_ exemplos** na estrutura de informações do [**fluxo de saída do MFT \_ \_ \_**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) . Esse sinalizador notifica a sessão de mídia de que a MFT aloca seus próprios exemplos de saída. Para alocar os exemplos de saída, o MFT executa as seguintes etapas:

1.  Crie uma matriz de textura 2D chamando [**ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). Na estrutura [**\_ \_ desc de D3D11 TEXTURE2D**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) , defina **matrizes** igual ao número de superfícies que o decodificador precisa. Isso inclui:
    -   Superfícies para quadros de referência.
    -   Superfícies para desentrelaçamento (três superfícies).
    -   Superfícies de que o decodificador precisa para o armazenamento em buffer.

    Os sinalizadores de associação (**BindFlags**) devem incluir o sinalizador de **\_ \_ decodificador de associação D3D11** e todos os sinalizadores de associação definidos por meio do atributo [MF \_ SA \_ D3D11 \_ BindFlags](mf-sa-d3d11-bindflags.md) nos atributos do fluxo de saída.
2.  Para cada superfície na matriz de textura, chame [**ID3D11VideoDevice:: CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) para criar uma exibição de saída de decodificador de vídeo. Durante a decodificação, essas exibições de saída serão passadas para o método [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) .
3.  Para cada superfície na matriz de textura, crie um exemplo de mídia da seguinte maneira:
    1.  Crie um buffer de mídia DXGI chamando a função [**MFCreateDXGISurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) . Passe o ponteiro [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e o deslocamento para cada elemento na matriz de textura. A função retorna um ponteiro [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
    2.  Crie um exemplo de mídia vazio chamando a função [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . Defina o parâmetro *pUnkSurface* igual a **NULL**. A função retorna um ponteiro [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
    3.  Chame [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para adicionar o buffer de mídia ao exemplo.

Você deve destruir todas as texturas que criar ao mesmo tempo, em vez de destruir apenas algumas e continuar a usar o lembrete.

## <a name="decoding"></a>Decodificação

Para criar o dispositivo decodificador, chame [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). O método retorna um ponteiro para a interface [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) . A decodificação deve ocorrer dentro do método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Em cada quadro, chame [**IMFDXGIDeviceManager:: TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) para testar a disponibilidade do dxgi. Se o dispositivo tiver sido alterado, o decodificador de software deverá recriar o dispositivo decodificador da seguinte maneira:

1.  Feche o identificador do dispositivo chamando [**IMFDXGIDeviceManager:: CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Libere todos os recursos associados ao dispositivo Direct3D 11 anterior, incluindo as interfaces [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder), [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext), [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)e [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) .
3.  Abra um novo identificador de dispositivo.
4.  Negocie uma nova configuração de decodificador, conforme descrito anteriormente em [Localizar uma configuração de decodificador](#find-a-decoder-configuration). Esta etapa é necessária porque os recursos do dispositivo podem ter sido alterados.
5.  Crie um novo dispositivo de decodificador.

Supondo que o identificador do dispositivo seja válido, o processo de decodificação funciona da seguinte maneira:

1.  Obtenha uma superfície disponível que não esteja em uso no momento. Inicialmente, todas as superfícies estão disponíveis.
2.  Consulte o exemplo de mídia para a interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Chame [**IMFTrackedSample:: Setalocador**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e forneça um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . (O decodificador de software deve implementar essa interface.) Quando o processador de vídeo libera o exemplo, o retorno de chamada será invocado. Use este retorno de chamada para acompanhar quais exemplos estão disponíveis no momento e quais estão em uso.
4.  Chame [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Passe os ponteiros para a interface [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) para o dispositivo decodificador e a interface [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) para a exibição de saída.
5.  Faça o seguinte uma ou mais vezes:
    1.  Chame [**ID3D11VideoContext:: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) para obter um buffer.
    2.  Preencha o buffer.
    3.  Chame [**ID3D11VideoContext:: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Chame [**ID3D11VideoContext:: SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Esse método instrui o dispositivo decodificador a executar as operações de decodificação no quadro.
6.  Chame [**ID3D11VideoContext::D ecoderendframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) para sinalizar o fim da decodificação do quadro atual.

O Direct3D 11 usa as mesmas estruturas de dados que a DXVA 2,0 para operações de decodificação. Para o conjunto original de perfis de DXVA (para H. 261, H. 263 e MPEG-2), essas estruturas de dados são descritas na [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Dentro de cada par de chamadas [**DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) e [**SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) , você pode chamar [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) várias vezes, mas apenas uma vez para cada tipo de buffer. Se você usar o mesmo tipo de buffer duas vezes sem chamar **SubmitDecoderBuffer**, os dados serão substituídos no buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
