---
description: Suporte ao DXVA 2.0 no Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Suporte ao DXVA 2.0 no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721917"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Suporte ao DXVA 2.0 no Media Foundation

Este tópico descreve como dar suporte à DXVA (Aceleração de Vídeo DirectX) 2.0 em uma transformação de Media Foundation (MFT) usando o Microsoft Direct3D 9 Especificamente, ele descreve a comunicação entre o decodificador e o renderdor de vídeo, que é mediado pelo carregador de topologia. Este tópico não descreve como implementar a decodificação DXVA.

No restante deste tópico, o termo *decodificador* refere-se ao decodificador MFT, que recebe vídeo compactado e saída de vídeo descompactado. O termo *dispositivo decodificador* refere-se a um acelerador de vídeo de hardware implementado pelo driver de gráficos.

> [!TIP]
> Para obter informações sobre a decodificação de vídeo do Microsoft Direct3D 11, consulte Support [Direct3D 11 Video Decoding in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Windows Os aplicativos da Store devem usar o Direct3D 11.

 

Aqui estão as etapas básicas que um decodificador deve executar para dar suporte ao DXVA 2.0 Media Foundation:

1.  Abra um alça para o dispositivo Direct3D 9.
2.  Encontre uma configuração do decodificador DXVA.
3.  Alocar buffers descompactados.
4.  Decodificar quadros.

Essas etapas são descritas mais detalhadamente no restante deste tópico.

## <a name="opening-a-direct3d-device-handle"></a>Abrindo um alça de dispositivo Direct3D

O MFT usa o gerenciador de dispositivos do Microsoft Direct3D para obter um handle para o dispositivo Direct3D 9. Para abrir o alça do dispositivo, execute as seguintes etapas:

1.  Exponha o [atributo \_ MF SA \_ D3D \_ AWARE](mf-sa-d3d-aware-attribute.md) com o valor **TRUE.** O carregador de topologia consulta esse atributo chamando [**IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Definir o atributo como **TRUE** notifica o carregador de topologia de que o MFT dá suporte a DXVA.
2.  Quando a negociação de formato é iniciada, o carregador de topologia chama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER.**](mft-message-set-d3d-manager.md) O *parâmetro ulParam* é um **ponteiro IUnknown** para o gerenciador de dispositivos Direct3D do renderador de vídeo. Consulte este ponteiro para a interface [**IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)
3.  Chame [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um handle para o dispositivo Direct3D do renderador.
4.  Chame [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passe a alça do dispositivo. Esse método retorna um ponteiro para a interface [**IDirectXVideoDecoderService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)
5.  Armazenar os ponteiros e o dispositivo em cache.

## <a name="finding-a-decoder-configuration"></a>Localizar uma configuração do decodificador

O MFT deve encontrar uma configuração compatível para o dispositivo decodificador DXVA. Execute as seguintes etapas dentro do [**método IMFTransform::SetInputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) depois de validar o tipo de entrada:

1.  Chame [**IDirectXVideoDecoderService::GetDecoderDeviceGuids.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids) Esse método retorna uma matriz de GUIDs do dispositivo decodificador.
2.  Loop pela matriz de GUIDs do decodificador para encontrar aqueles aos quais o decodificador dá suporte. Por exemplo, para um decodificador MPEG-2, você procuraria **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou **DXVA2 \_ ModeMPEG2 \_ VLD**.

3.  Quando você encontrar um GUID de dispositivo de decodificador candidato, passe o GUID para o método [**IDirectXVideoDecoderService::GetDecoderRenderTargets.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Esse método retorna uma matriz de formatos de destino de renderização, especificados como **valores D3DFORMAT.**
4.  Loop pelos formatos de destino de renderização e procure um formato com suporte pelo decodificador.
5.  Chame [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passe o mesmo GUID do dispositivo decodificador, juntamente com uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que descreve o formato de saída proposto. O método retorna uma matriz de [**estruturas DXVA2 \_ ConfigPictureDecode.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) Cada estrutura descreve uma configuração possível para o dispositivo decodificador. Procure uma configuração compatível com o decodificador.
6.  Armazene o formato e a configuração de destino de renderização.

No método [**IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retorne um formato de vídeo descompactado, com base no formato de destino de renderização proposto.

No método [**IMFTransform::SetOutputType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) verifique o tipo de mídia em relação ao formato de destino de renderização.

### <a name="fallback-to-software-decoding"></a>Fallback para Decodificação de Software

Se o MFT não puder encontrar uma configuração DXVA (por exemplo, se o driver de gráficos não tiver os recursos certos), ele deverá retornar o código de erro **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE** dos métodos [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) e [**SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) O carregador de topologia responderá enviando a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) com o valor **NULL** para o *parâmetro ulParam.* O MFT deve liberar seu ponteiro para a interface [**IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) O carregador de topologia, em seguida, negociará o tipo de mídia e o MFT poderá usar a decodificação de software.

## <a name="allocating-uncompressed-buffers"></a>Alocando buffers descompactados

No DXVA 2.0, o decodificador é responsável por alocar superfícies Direct3D para usar como buffers de vídeo descompactados. O decodificador deve alocar três superfícies para o EVR usar para desintercalação. Esse número é fixo, porque Media Foundation fornece uma maneira para o EVR especificar quantas superfícies o driver gráfico requer para desintercalar. Três superfícies devem ser suficientes para qualquer driver.

No método [**IMFTransform::GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) de definido o sinalizador **MFT \_ OUTPUT STREAM PROVIDES \_ \_ \_ SAMPLES** na estrutura [**MFT OUTPUT STREAM \_ \_ \_ INFO.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Esse sinalizador notifica a Sessão de Mídia de que o MFT aloca seus próprios exemplos de saída.

Para criar as superfícies, chame [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (A interface [**IDirectXVideoDecoderService herda**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) esse método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Você pode fazer isso em [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype), depois de localizar o formato de destino de renderização.

Para cada superfície, chame [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) para criar um exemplo de mídia para manter a superfície. O método retorna um ponteiro para a interface [**IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="decoding"></a>Decodificação

Para criar o dispositivo de decodificador, chame [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). O método retorna um ponteiro para a interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) do dispositivo decodificador.

A decodificação deve ocorrer dentro do [**método IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Em cada quadro, chame [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para testar o handle do dispositivo. Se o dispositivo tiver sido alterado, o método **retornará DXVA2 \_ E NEW VIDEO \_ \_ \_ DEVICE**. Se isso ocorrer, faça o seguinte:

1.  Feche o alçamento do dispositivo chamando [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere os [**ponteiros IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) [**e IDirectXVideoDecoder.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)
3.  Abra uma nova alça de dispositivo.
4.  Negociar uma nova configuração do decodificador, conforme descrito em "Encontrando uma configuração de decodificador" anteriormente nesta página.
5.  Crie um novo dispositivo de decodificador.

Supondo que o handle do dispositivo seja válido, o processo de decodificação funciona da seguinte forma:

1.  Obter uma superfície disponível que não está em uso no momento. (Inicialmente, todas as superfícies estão disponíveis.)
2.  Consulte o exemplo de mídia para a interface [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)
3.  Chame [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e forneça um ponteiro para a interface [**IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementada pelo decodificador. Quando o renderador de vídeo liberar o exemplo, o retorno de chamada do decodificador será invocado.
4.  Chame [**IDirectXVideoDecoder::BeginFrame.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)
5.  Faça o seguinte uma ou mais vezes:
    1.  Chame [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obter um buffer de decodificador DXVA.
    2.  Preencha o buffer.
    3.  Chame [**IDirectXVideoDecoder::ReleaseBuffer.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)
    4.  Chame [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para executar as operações de decodificação no quadro.

O DXVA 2.0 usa as mesmas estruturas de dados que o DXVA 1.0 para operações de decodificação. Para o conjunto original de perfis DXVA (para H.261, H.263 e MPEG-2), essas estruturas de dados são descritas na especificação [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

Em cada par de [**chamadas BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)Execute, você pode chamar GetBuffer várias vezes, mas apenas uma vez para / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) cada tipo de buffer DXVA. [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) Se você chamá-lo duas vezes com o mesmo tipo de buffer, substituirá os dados.

Use o retorno de chamada do [**método SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (etapa 3) para controlar quais amostras estão disponíveis no momento e quais estão em uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 
