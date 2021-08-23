---
description: Negociação de tipo de mídia EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negociação de tipo de mídia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974485"
---
# <a name="evr-media-type-negotiation"></a>Negociação de tipo de mídia EVR

Este tópico descreve como o EVR (renderador de vídeo aprimorado) valida os tipos de mídia.

-   Para o DirectShow EVR, a negociação de tipo ocorre quando os pinos do filtro são conectados.

-   Para o sink de mídia EVR, os tipos de mídia são definidos por meio da interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nos sinks de fluxo. Normalmente, o carregador de topologia negocia os tipos de mídia, embora o aplicativo também possa definir os tipos de mídia diretamente.

O EVR não relata nenhum tipo de mídia preferencial. O cliente deve testar tipos de mídia até encontrar um tipo aceitável. O tipo de mídia para o fluxo de referência deve ser definido antes que os tipos possam ser definidos em qualquer um dos substreams.

Para o fluxo de referência, o mixer EVR obtém uma lista de formatos de destino de renderização de DXVA (Aceleração de Vídeo DirectX) compatíveis. O apresentador de EVR usa essa lista para selecionar o formato da cadeia de permuta do Direct3D. Se nenhum formato de destino de renderização compatível puder ser encontrado, o EVR rejeitará o tipo de mídia.

Para os substreams, o mixer EVR consulta se o dispositivo DXVA dá suporte a esse formato de substream em combinação com o formato de destino de renderização selecionado para o fluxo de referência. Como resultado, os formatos de substream disponíveis podem mudar dependendo do fluxo de referência.

Este é o processo em mais detalhes. Esses detalhes não são importantes para a maioria dos aplicativos, mas podem ser úteis se você estiver escrevendo um mixer ou um apresentador personalizado.

Para o fluxo de referência, a negociação ocorre da seguinte forma:

1.  O EVR chama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.

2.  O mixer converte o tipo de mídia em uma descrição DXVA 2.0, usando a estrutura [**DXVA2 \_ VideoDesc.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc)

3.  O mixer chama [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) para obter uma lista de GUIDs do processador de vídeo.

4.  Para cada GUID do processador de vídeo, o mixer chama [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) para obter os formatos de destino de renderização com suporte.

5.  O EVR chama [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) no apresentador com a mensagem MFVP \_ \_ MESSAGE INVALIDATEMEDIATYPE. Essa mensagem faz com que o apresentador selecione um novo formato.

6.  O apresentador chama [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma lista dos formatos de saída disponíveis do mixer. O mixer gera essa lista dos formatos obtidos na etapa 4.

7.  O apresentador seleciona um formato e chama [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) no mixer.

Para substreams, o processo é mais simples:

1.  O EVR chama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) no mixer.

2.  O mixer chama [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) para obter uma lista de formatos de substream disponíveis.

3.  Se o formato proposto estiver contido nessa lista, o EVR aceitará o tipo de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> </dl>

 

 



