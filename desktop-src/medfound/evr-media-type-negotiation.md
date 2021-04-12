---
description: Negociação de tipo de mídia EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negociação de tipo de mídia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297940"
---
# <a name="evr-media-type-negotiation"></a>Negociação de tipo de mídia EVR

Este tópico descreve como o processador de vídeo avançado (EVR) valida os tipos de mídia.

-   Para o filtro EVR do DirectShow, a negociação do tipo ocorre quando os Pins do filtro são conectados.

-   Para o coletor de mídia do EVR, os tipos de mídia são definidos por meio da interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nos coletores de fluxo. Normalmente, o carregador de topologia negocia os tipos de mídia, embora o aplicativo também possa definir os tipos de mídia diretamente.

O EVR não relata nenhum tipo de mídia preferencial. O cliente deve testar os tipos de mídia até encontrar um tipo aceitável. O tipo de mídia para o fluxo de referência deve ser definido antes que os tipos possam ser definidos em qualquer um dos subfluxos.

Para o fluxo de referência, o mixer EVR Obtém uma lista de formatos de destino de renderização DXVA (DirectX Video Acceleration) compatíveis. O apresentador EVR usa essa lista para selecionar o formato da cadeia de permuta do Direct3D. Se nenhum formato de destino de renderização compatível puder ser encontrado, o EVR rejeitará o tipo de mídia.

Para os subfluxos, o mixer EVR consulta se o dispositivo DXVA dá suporte a esse formato de Subfluxo em combinação com o formato de destino de renderização selecionado para o fluxo de referência. Como resultado, os formatos de Subfluxo disponíveis podem mudar dependendo do fluxo de referência.

Aqui está o processo em mais detalhes. Esses detalhes não são importantes para a maioria dos aplicativos, mas podem ser úteis se você estiver escrevendo um mixer ou apresentador personalizado.

Para o fluxo de referência, a negociação ocorre da seguinte maneira:

1.  O EVR chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.

2.  O mixer converte o tipo de mídia em uma descrição de DXVA 2,0, usando a estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .

3.  O mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obter uma lista de GUIDs de processador de vídeo.

4.  Para cada GUID de processador de vídeo, o mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obter os formatos de destino de renderização com suporte.

5.  O EVR chama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) no apresentador com a mensagem MFVP \_ Message \_ INVALIDATEMEDIATYPE. Essa mensagem faz com que o apresentador selecione um novo formato.

6.  O apresentador chama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma lista de formatos de saída disponíveis do mixer. O mixer gera essa lista com base nos formatos obtidos na etapa 4.

7.  O apresentador seleciona um formato e chama [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) no mixer.

Para subfluxos, o processo é mais simples:

1.  O EVR chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.

2.  O mixer chama [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obter uma lista de formatos de Subfluxo disponíveis.

3.  Se o formato proposto estiver contido nessa lista, o EVR aceitará o tipo de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



