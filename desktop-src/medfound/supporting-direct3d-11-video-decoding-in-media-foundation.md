---
description: Este tópico descreve como dar suporte ao Microsoft Direct3D 11 em um Microsoft Media Foundation decodificador.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Suporte à decodificação de vídeo do Direct3D 11 Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95a1d1bc1dd9987fe59fe807e56aa9af1ea4ad597b72c077906483d623e11e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972875"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Suporte à decodificação de vídeo do Direct3D 11 Media Foundation

Este tópico descreve como dar suporte ao Microsoft Direct3D 11 em um Microsoft Media Foundation decodificador. Especificamente, ele descreve a comunicação entre o decodificador e o renderista de vídeo. Este tópico não descreve como implementar as operações de decodificação.

-   [Visão geral](#overview)
-   [Abrir um alça de dispositivo](#open-a-device-handle)
-   [Encontrar uma configuração do decodificador](#find-a-decoder-configuration)
-   [Fallback para Decodificação de Software](#fallback-to-software-decoding)
-   [Alocando buffers descompactados](#allocating-uncompressed-buffers)
-   [Decodificação](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

No restante deste tópico, os seguintes termos são usados:

-   **Decodificador de software**. O decodificador de software é a Media Foundation transformação (MFT) que recebe amostras de vídeo compactadas e saídas de quadros de vídeo descompactados.
-   **Dispositivo de decodificador**. O dispositivo decodificador é o acelerador de vídeo e é implementado pelo driver de gráficos. O dispositivo decodificador executa operações de decodificação aceleradas.
-   **Pipeline**. O pipeline hospeda o decodificador de software e fornece buffers de e para o decodificador de software. Dependendo do aplicativo, o pipeline pode ser a Sessão de [Mídia,](media-session.md) [o](source-reader.md)Leitor de Origem ou o código do aplicativo que chama diretamente para o MFT.

Para executar a decodificação usando o Direct3D 11, o decodificador de software deve ter um ponteiro para um dispositivo Direct3D 11. O dispositivo Direct3D 11 é criado externamente para o decodificador de software. Em um [cenário de Sessão de](media-session.md) Mídia, o renderador de vídeo cria o dispositivo Direct3D 11. Em um [cenário de Leitor de](source-reader.md) Origem, normalmente o aplicativo cria o dispositivo Direct3D 11.

O DXGI Gerenciador de Dispositivos é usado para compartilhar o Direct3D 11 entre componentes. O DXGI Gerenciador de Dispositivos expõe a interface [**IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) O pipeline define o **ponteiro IMFDXGIDeviceManager** no decodificador de software enviando a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md)

O diagrama a seguir mostra a relação entre o decodificador de software, o Direct3D 11 e o pipeline.

![um diagrama que mostra o decodificador de software e o gerenciador de dispositivos dxgi.](images/d3d11video01.png)

Aqui estão as etapas básicas que um decodificador de software deve executar para dar suporte ao Direct3D 11 Media Foundation:

1.  Abra um alça para o dispositivo Direct3D 11.
2.  Encontre uma configuração do decodificador.
3.  Alocar buffers descompactados.
4.  Decodificar quadros.

Essas etapas são descritas mais detalhadamente no restante deste tópico.

## <a name="open-a-device-handle"></a>Abrir um alça de dispositivo

O decodificador MFT usa o gerenciador de dispositivos DXGI para obter um handle para o dispositivo Direct3D 11. Para abrir o alça do dispositivo, execute as seguintes etapas:

1.  O MFT do decodificador deve expor o [atributo \_ MF SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) com o **valor TRUE.**
2.  O Carregador de Topologia consulta esse atributo chamando [**IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) O valor **TRUE** indica que o MFT dá suporte ao Direct3D 11.
3.  O Carregador de Topologia chama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) O *parâmetro ulParam* é um [**ponteiro IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para o gerenciador de dispositivos DXGI. Consulte este ponteiro para a interface [**IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  Chame [**IMFDXGIDeviceManager::OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) para obter um handle para o dispositivo Direct3D 11.
5.  Para obter um ponteiro para o dispositivo Direct3D 11, chame [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Passe o handle do dispositivo e o valor **\_ IID ID3D11Device**. O método retorna um ponteiro para a [**interface ID3D11Device.**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)
6.  Para obter um ponteiro para o acelerador de vídeo, chame [**IMFDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) novamente. Desta vez, passe o handle do dispositivo e o valor **\_ IID ID3D11VideoDevice**. O método retorna um ponteiro para a interface [**ID3D11VideoDevice.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)
7.  Chame [**ID3D11Device::GetImmediateContext para**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) obter um [**ponteiro ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext)
8.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no [**ID3D11DeviceContext para**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) obter um [**ponteiro ID3D11VideoContext.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)
9.  É recomendável usar a proteção multi-thread no contexto do dispositivo para evitar problemas de deadlock que às vezes podem ocorrer quando você chama [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) [**ou ID3D11VideoContext::ReleaseDecoderBuffer.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) Para definir a proteção multi-thread, primeiro chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) [**em ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) para obter um [**ponteiro ID3D10Multithread.**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) Em seguida, [**chame ID3D10Multithread::SetMultithreadProtected, passando**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected) **true** para *bMTProtect.*

## <a name="find-a-decoder-configuration"></a>Encontrar uma configuração do decodificador

Para executar a decodificação, o decodificador de software deve encontrar uma configuração compatível com o dispositivo decodificador, incluindo um formato de destino de renderização. Essa etapa ocorre dentro do [**método IMFTransform::SetInputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) da seguinte forma.

1.  Valide o tipo de mídia de entrada. Se o tipo for rejeitado, ignore as etapas restantes e retorne um código de erro.
2.  Chame [**ID3D11VideoDevice::GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) para obter o número de perfis com suporte.
3.  Chame [**ID3D11VideoDevice::GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) para enumerar os perfis e obter os GUIDs de perfil.
4.  Procure um GUID de perfil que corresponde ao formato de vídeo e aos recursos do decodificador de software. Por exemplo, um decodificador MPEG-2 procuraria O PERFIL **DO DECODIFICADOR D3D11 \_ \_ \_ MPEG2 \_ MOCOMP**,**D3D11 IDCT DO PERFIL DO \_ \_ \_ DECODIFICADOR MPEG2 \_** e **D3D11 \_ PERFIL DO DECODIFICADOR \_ \_ MPEG2 \_ VLD**.
5.  Se um GUID de decodificador adequado for encontrado, verifique o formato de saída chamando o método [**ID3D11VideoDevice::CheckVideoDecoderFormat.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) Passe o GUID do decodificador e um **valor DXGI \_ FORMAT** que especifica o formato de destino de renderização.
6.  Em seguida, encontre uma configuração adequada para o decodificador.
    1.  Chame [**ID3D11VideoDevice::GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) para obter o número de configurações do decodificador. Passe o mesmo GUID do dispositivo de decodificador, juntamente com uma estrutura [**D3D11 \_ VIDEO \_ DECODER \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) que descreve o formato de destino de renderização proposto.
    2.  Chame [**ID3D11VideoDevice::GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) para enumerar as configurações do decodificador.

No método [**IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retorne um formato de vídeo descompactado com base no formato de destino de renderização proposto.

No método [**IMFTransform::SetOutputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) verifique o tipo de mídia em relação ao formato de destino de renderização.

## <a name="fallback-to-software-decoding"></a>Fallback para Decodificação de Software

O MFT pode não conseguir encontrar uma configuração. Por exemplo, o driver de gráficos pode não dar suporte aos recursos corretos. Nesse caso, o MFT deve voltar para a decodificação de software, da seguinte forma.

1.  Os [**métodos SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) e [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) devem retornar **MF E \_ \_ UNSUPPORTED \_ D3D \_ TYPE**.
2.  Em resposta, o Carregador de Topologia enviará a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) com o valor **NULL** para o *parâmetro ulParam.*
3.  O MFT libera seu ponteiro para a interface [**IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)
4.  O Carregador de Topologia renegocia o tipo de mídia.

Neste ponto, o MFT pode usar a decodificação de software.

## <a name="allocating-uncompressed-buffers"></a>Alocando buffers descompactados

O decodificador é responsável por alocar texturas direct3D 11 para usar como buffers de vídeo descompactados. O atributo [MF \_ SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ COUNT](mf-sa-minimum-output-sample-count.md) nos atributos de fluxo de saída (consulte [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) é usado para determinar quantas superfícies o decodificador deve alocar para o renderador de vídeo usar para desintercalar . Um decodificador deve usar esse valor delimitando-o para alguns limites superiores e inferiores razoáveis, por exemplo, 3 a 32. Para conteúdo progressivo, consulte [MF \_ SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ PROGRESSIVE](mf-sa-minimum-output-sample-count-progressive.md).

No método [**IMFTransform::GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) de definido o sinalizador **MFT \_ OUTPUT STREAM PROVIDES \_ \_ \_ SAMPLES** na estrutura [**MFT OUTPUT STREAM \_ \_ \_ INFO.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) Esse sinalizador notifica a Sessão de Mídia de que o MFT aloca seus próprios exemplos de saída. Para alocar os exemplos de saída, o MFT executa as seguintes etapas:

1.  Crie uma matriz de textura 2D chamando [**ID3D11Device::CreateTexture2D.**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d) Na estrutura [**D3D11 \_ TEXTURE2D \_ DESC,**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) de conjunto **ArraySize** igual ao número de superfícies de que o decodificador precisa. Isso inclui:
    -   Superfícies para quadros de referência.
    -   Superfícies para desintercalação (três superfícies).
    -   Revela que o decodificador precisa para buffer.

    Os sinalizadores de associação (**BindFlags**) devem incluir o sinalizador **D3D11 \_ BIND \_ DECODER** e todos os sinalizadores de associação definidos por meio do atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) nos atributos de fluxo de saída.
2.  Para cada superfície na matriz de textura, chame [**ID3D11VideoDevice::CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) para criar uma exibição de saída do decodificador de vídeo. Durante a decodificação, essas exibições de saída serão passadas para o [**método ID3D11VideoContext::D ecoderBeginFrame.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)
3.  Para cada superfície na matriz de textura, crie um exemplo de mídia da seguinte forma:
    1.  Crie um buffer de mídia DXGI chamando a [**função MFCreateDXGISurfaceBuffer.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) Passe o ponteiro [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e o deslocamento para cada elemento na matriz de textura. A função retorna um [**ponteiro IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
    2.  Crie um exemplo de mídia vazio chamando a [**função MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) De definir *o parâmetro pUnkSurface* igual a **NULL.** A função retorna um [**ponteiro IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
    3.  Chame [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para adicionar o buffer de mídia ao exemplo.

Você deve destruir todas as texturas que cria ao mesmo tempo, em vez de destruir apenas algumas e continuar a usar o lembrete.

## <a name="decoding"></a>Decodificação

Para criar o dispositivo decodificador, chame [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). O método retorna um ponteiro para a interface [**ID3D11VideoDecoder.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) A decodificação deve ocorrer dentro do [**método IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Em cada quadro, chame [**IMFDXGIDeviceManager::TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) para testar a disponibilidade do DXGI. Se o dispositivo tiver sido alterado, o decodificador de software deverá recriar o dispositivo decodificador, da seguinte forma:

1.  Feche o alçamento do dispositivo chamando [**IMFDXGIDeviceManager::CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Libere todos os recursos associados ao dispositivo Direct3D 11 anterior, incluindo as interfaces [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder), [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext), [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)e [**ID3D11VideoDecoderOutputView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview)
3.  Abra uma nova alça de dispositivo.
4.  Negociar uma nova configuração do decodificador, conforme descrito anteriormente em [Encontrar uma configuração do decodificador](#find-a-decoder-configuration). Essa etapa é necessária porque os recursos do dispositivo podem ter sido alterados.
5.  Crie um novo dispositivo de decodificador.

Supondo que o handle do dispositivo seja válido, o processo de decodificação funciona da seguinte forma:

1.  Obter uma superfície disponível que não está em uso no momento. Inicialmente, todas as superfícies estão disponíveis.
2.  Consulte o exemplo de mídia para a interface [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Chame [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e forneça um ponteiro para a interface [**IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) (O decodificador de software deve implementar essa interface.) Quando o renderador de vídeo liberar o exemplo, o retorno de chamada será invocado. Use esse retorno de chamada para controlar quais amostras estão disponíveis no momento e quais estão em uso.
4.  Chame [**ID3D11VideoContext::D ecoderBeginFrame.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) Passe os ponteiros para a interface [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) para o dispositivo decodificador e a interface [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) para a exibição de saída.
5.  Faça o seguinte uma ou mais vezes:
    1.  Chame [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) para obter um buffer.
    2.  Preencha o buffer.
    3.  Chame [**ID3D11VideoContext::ReleaseDecoderBuffer.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)
    4.  Chame [**ID3D11VideoContext::SubmitDecoderBuffer.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) Esse método instrui o dispositivo decodificador a executar as operações de decodificação no quadro.
6.  Chame [**ID3D11VideoContext::D ecoderEndFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) para sinalizar o fim da decodificação para o quadro atual.

O Direct3D 11 usa as mesmas estruturas de dados que o DXVA 2.0 para operações de decodificação. Para o conjunto original de perfis DXVA (para H.261, H.263 e MPEG-2), essas estruturas de dados são descritas na especificação [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

Em cada par de chamadas [**de DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) e [**SubmitDecoderBuffer,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) você pode chamar [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) várias vezes, mas apenas uma vez para cada tipo de buffer. Se você usar o mesmo tipo de buffer duas vezes sem chamar **SubmitDecoderBuffer,** substituirá os dados no buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Aceleração de vídeo do DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
