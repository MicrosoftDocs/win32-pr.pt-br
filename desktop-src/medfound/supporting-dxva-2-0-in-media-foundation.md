---
description: Suporte a DXVA 2,0 no Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Suporte a DXVA 2,0 no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce144c24a1aeeda6281ddb423757f3e339903440
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105756112"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Suporte a DXVA 2,0 no Media Foundation

Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em uma Media Foundation transformação (MFT) usando o Microsoft Direct3D 9 especificamente, ele descreve a comunicação entre o decodificador e o processador de vídeo, que é mediado pelo carregador de topologia. Este tópico não descreve como implementar a decodificação de DXVA.

No restante deste tópico, o termo *decodificador* refere-se ao MFT do decodificador, que recebe vídeo compactado e gera vídeo descompactado. O termo *dispositivo decodificador* refere-se a um acelerador de vídeo de hardware implementado pelo driver de gráficos.

> [!TIP]
> Para obter informações sobre a decodificação de vídeo do Microsoft Direct3D 11, consulte [dando suporte à decodificação de vídeo do Direct3D 11 em Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Os aplicativos da Windows Store devem usar o Direct3D 11.

 

Aqui estão as etapas básicas que um decodificador deve executar para dar suporte a DXVA 2,0 no Media Foundation:

1.  Abra um identificador para o dispositivo Direct3D 9.
2.  Localize uma configuração de decodificador DXVA.
3.  Aloque buffers descompactados.
4.  Decodificar quadros.

Essas etapas são descritas mais detalhadamente no restante deste tópico.

## <a name="opening-a-direct3d-device-handle"></a>Abrindo um identificador de dispositivo Direct3D

O MFT usa o Microsoft Direct3D Device Manager para obter um identificador para o dispositivo Direct3D 9. Para abrir o identificador do dispositivo, execute as seguintes etapas:

1.  Expor o atributo de [ \_ \_ \_ reconhecimento de D3D SA do MF](mf-sa-d3d-aware-attribute.md) com o valor **true**. O carregador de topologia consulta esse atributo chamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Definir o atributo como **true** notifica o carregador de topologia que o MFT dá suporte a DXVA.
2.  Quando a negociação de formato começa, o carregador de topologia chama [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**MFT do conjunto de mensagens do \_ \_ \_ \_ Gerenciador de D3D**](mft-message-set-d3d-manager.md) . O parâmetro *ulParam* é um ponteiro **IUnknown** para o Gerenciador de dispositivos Direct3D do processador de vídeo. Consulte este ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Chame [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um identificador para o dispositivo Direct3D do renderizador.
4.  Chame [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passe o identificador do dispositivo. Esse método retorna um ponteiro para a interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Armazene os ponteiros e o identificador do dispositivo em cache.

## <a name="finding-a-decoder-configuration"></a>Encontrando uma configuração de decodificador

O MFT deve encontrar uma configuração compatível para o dispositivo de decodificador DXVA. Execute as seguintes etapas dentro do método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , depois de validar o tipo de entrada:

1.  Chame [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Esse método retorna uma matriz de GUIDs de dispositivo do decodificador.
2.  Faça um loop através da matriz de GUIDs do decodificador para localizar os que o decodificador suporta. Por exemplo, para um decodificador MPEG-2, você procurará **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou **DXVA2 \_ ModeMPEG2 \_** VLD.

3.  Quando você encontrar um GUID de dispositivo de decodificador candidato, passe o GUID para o método [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Esse método retorna uma matriz de formatos de destino de renderização, especificados como valores de **D3DFORMAT** .
4.  Faça um loop pelos formatos de destino de renderização e procure por um formato com suporte pelo decodificador.
5.  Chame [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passe o mesmo GUID do dispositivo decodificador, junto com uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que descreve o formato de saída proposto. O método retorna uma matriz de estruturas [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Cada estrutura descreve uma configuração possível para o dispositivo decodificador. Procure uma configuração que o decodificador dê suporte.
6.  Armazene o formato de destino de renderização e a configuração.

No método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , retorne um formato de vídeo descompactado, com base no formato de destino de renderização proposto.

No método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , verifique o tipo de mídia em relação ao formato de destino de renderização.

### <a name="fallback-to-software-decoding"></a>Fallback para decodificação de software

Se o MFT não puder encontrar uma configuração de DXVA (por exemplo, se o driver de gráficos não tiver os recursos corretos), ele deverá retornar o código de erro **MF \_ e o \_ \_ \_ tipo de D3D sem suporte** dos métodos [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) e [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . O carregador de topologia responderá enviando a mensagem [**MFT do conjunto de mensagens do \_ \_ \_ \_ Gerenciador de D3D**](mft-message-set-d3d-manager.md) com o valor **NULL** para o parâmetro *ulParam* . O MFT deve liberar seu ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . O carregador de topologia renegociará o tipo de mídia e o MFT poderá usar a decodificação de software.

## <a name="allocating-uncompressed-buffers"></a>Alocando buffers descompactados

No DXVA 2,0, o decodificador é responsável por alocar superfícies do Direct3D para usar como buffers de vídeo não compactados. O decodificador deve alocar 3 superfícies para o EVR usar para desentrelaçar. Esse número é fixo, porque Media Foundation não fornece uma maneira para o EVR especificar quantas superfícies o driver gráfico requer para desentrelaçar. Três superfícies devem ser suficientes para qualquer driver.

No método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , defina o **fluxo de saída do MFT fornece um sinalizador de \_ \_ \_ \_ exemplos** na estrutura de informações do [**fluxo de saída do MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Esse sinalizador notifica a sessão de mídia de que a MFT aloca seus próprios exemplos de saída.

Para criar as superfícies, chame [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (A interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) herda esse método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Você pode fazer isso em [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype), depois de localizar o formato de destino de renderização.

Para cada superfície, chame [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) para criar um exemplo de mídia para manter a superfície. O método retorna um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="decoding"></a>Decodificação

Para criar o dispositivo decodificador, chame [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). O método retorna um ponteiro para a interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) do dispositivo decodificador.

A decodificação deve ocorrer dentro do método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Em cada quadro, chame [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para testar o identificador do dispositivo. Se o dispositivo tiver sido alterado, o método **retornará \_ DXVA2 \_ E \_ novo \_ dispositivo de vídeo**. Se isso ocorrer, faça o seguinte:

1.  Feche o identificador do dispositivo chamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere os ponteiros [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Abra um novo identificador de dispositivo.
4.  Negocie uma nova configuração de decodificador, conforme descrito em "encontrando uma configuração de decodificador" anteriormente nesta página.
5.  Crie um novo dispositivo de decodificador.

Supondo que o identificador do dispositivo seja válido, o processo de decodificação funciona da seguinte maneira:

1.  Obtenha uma superfície disponível que não esteja em uso no momento. (Inicialmente, todas as superfícies estão disponíveis.)
2.  Consulte o exemplo de mídia para a interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Chame [**IMFTrackedSample:: Setalocador**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) e forneça um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , implementado pelo decodificador. Quando o processador de vídeo libera o exemplo, o retorno de chamada do decodificador será invocado.
4.  Chame [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Faça o seguinte uma ou mais vezes:
    1.  Chame [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obter um buffer de decodificador de DXVA.
    2.  Preencha o buffer.
    3.  Chame [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Chame [**IDirectXVideoDecoder:: execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para executar as operações de decodificação no quadro.

O DXVA 2,0 usa as mesmas estruturas de dados que a DXVA 1,0 para operações de decodificação. Para o conjunto original de perfis de DXVA (para H. 261, H. 263 e MPEG-2), essas estruturas de dados são descritas na [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Em cada par de [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / chamadas de [**execução**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, você pode chamar [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) várias vezes, mas apenas uma vez para cada tipo de buffer de DXVA. Se você chamá-lo duas vezes com o mesmo tipo de buffer, os dados serão substituídos.

Use o retorno de chamada do método [**Setalocador**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (etapa 3) para controlar quais exemplos estão disponíveis no momento e quais estão em uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
