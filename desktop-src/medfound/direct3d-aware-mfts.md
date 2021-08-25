---
description: Este tópico descreve como implementar uma transformação de Media Foundation com reconhecimento de Direct3D (MFT) para vídeo.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958727"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

Este tópico descreve como implementar uma transformação de Media Foundation *com reconhecimento de Direct3D* (MFT) para vídeo.

Um MFT de vídeo é considerado *com reconhecimento de Direct3D* se ele puder processar exemplos que contenham superfícies de Direct3D. O motivo típico para dar suporte ao Direct3D em um MFT de vídeo é habilitar a decodificação acelerada por hardware, usando a DXVA (aceleração de vídeo do DirectX).

Este tópico descreve as etapas necessárias para tornar o seu MFT com reconhecimento de Direct3D. Este tópico não aborda a mecânica da decodificação de DXVA. Para obter informações sobre o DXVA, consulte [aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> a partir do Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) pode ser usado em vez do [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). para aplicativos da Windows Store, você deve usar o **IMFDXGIDeviceManager** e o Microsoft Direct3D 11. Para obter mais informações, consulte as [APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implemente o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Esse método retorna um ponteiro para um repositório de atributos.
2.  O MFT deve definir o valor do atributo [**de \_ \_ \_ reconhecimento de D3D da SA MF**](mf-sa-d3d-aware-attribute.md) como **true** em seu próprio repositório de atributos. a partir do Windows 8, se usar o Direct3D 11, use o [D3D11 do MF \_ SA com \_ \_ reconhecimento](mf-sa-d3d11-aware.md).
3.  Durante a negociação de formato, se o atributo de [**\_ \_ \_ reconhecimento de D3D Sa**](mf-sa-d3d-aware-attribute.md) (ou [MF \_ SA \_ D3D11 \_ ciente](mf-sa-d3d11-aware.md) se estiver usando o Direct3D 11) for **verdadeiro**, o cliente poderá enviar a mensagem do Gerenciador de D3D para o conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md) O parâmetro de evento *ulParam* é um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . a partir do Windows 8, você pode usar [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) em vez de **IDirect3DDeviceManager9**. O cliente não é necessário para enviar esta mensagem.
4.  O MFT chama [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) para consultar o serviço DXVA necessário. a partir do Windows 8, se [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) foi usado, o MFT chama [**IMFDXGIDeviceManager:: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Normalmente, um decodificador consultaria [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice), e um processador de vídeo consultaria [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  Supondo que a etapa anterior seja bem-sucedida, os métodos [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) devem retornar formatos compatíveis com DXVA.
6.  O cliente configura os tipos de mídia no MFT. Se um tipo de mídia não for compatível com o DXVA, o MFT deverá retornar o código de erro **MF \_ E o \_ \_ \_ tipo de D3D sem suporte**.
7.  Neste ponto, há duas opções, dependendo se o cliente encontra um formato de DXVA adequado.
    -   Se o cliente configurar com êxito um formato DXVA, ele poderá começar a ser processado. Neste ponto, o MFT pode usar o DXVA para processamento ou fazer fallback para o processamento de software.
    -   Como alternativa, se o cliente não encontrar um formato de DXVA aceitável, o cliente poderá enviar outra mensagem de [**MFT do \_ \_ \_ \_ Gerenciador de D3D**](mft-message-set-d3d-manager.md) , desta vez definindo *ulParam* como **NULL**. O MFT deve liberar o ponteiro [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (o ponteiro [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , se **IMFDXGIDeviceManager** foi usado) e quaisquer outras interfaces de DXVA, e reverter para o processamento de software. Neste ponto, o MFT não deve usar o processamento de DXVA.

Um MFT com reconhecimento de Direct3D deve estar preparado para manipular exemplos que contêm uma superfície do Direct3D. O exemplo conterá exatamente um buffer de mídia. Para obter a superfície do Direct3D do buffer, chame a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e especifique o serviço do **\_ \_ serviço de buffer do Mr** . Para obter mais informações, consulte [buffer de superfície DirectX](directx-surface-buffer.md).

Uma MFT que usa o DXVA deve alocar seus próprios exemplos de saída, da seguinte maneira:

1.  No método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , defina o **fluxo de saída do MFT fornece um sinalizador de \_ \_ \_ \_ exemplos** .
2.  Crie um pool de superfícies de DXVA, conforme descrito na especificação DXVA.
3.  Crie amostras de mídia chamando [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

O MFT deve sempre dar suporte ao processamento de software como um fallback, porque o processamento de DXVA pode não estar disponível, por vários motivos:

-   A GPU pode não dar suporte a DXVA.
-   O cliente não pode usar o Direct3D.
-   Os perfis de DXVA não estão definidos para cada formato de vídeo.

Um MFT com reconhecimento de Direct3D deve ter um único fluxo de saída. Ele não pode ter várias saídas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



