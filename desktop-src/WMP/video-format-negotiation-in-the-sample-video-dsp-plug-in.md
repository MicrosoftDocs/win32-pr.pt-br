---
title: Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo
description: Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, negociação de formato de vídeo
- Plug-ins do DSP, negociação de formato de vídeo
- plug-ins de DSP de vídeo, negociação de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292251"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo

Antes de o Windows Media Player inserir um plug-in de DSP de vídeo na cadeia de sinais, o Player deve determinar se o plug-in pode processar o vídeo que está sendo reproduzido. O processo pelo qual o plug-in e o Player se comunicam sobre formatos de vídeo com suporte é chamado de negociação de formato.

## <a name="providing-the-supported-input-and-output-types"></a>Fornecendo os tipos de entrada e saída com suporte

Se o plug-in do DSP estiver agindo como um DMO (objeto de mídia do DirectX), o Player consultará o plug-in sobre seus formatos com suporte fazendo uma sequência de chamadas para **IMediaObject:: GetInputType** e **IMediaObject:: GetOutputType**.

Se o plug-in do DSP estiver agindo como uma Media Foundation transformação (MFT), o Player consultará o plug-in sobre seus formatos com suporte fazendo uma sequência de chamadas para **IMFTransform:: GetInputAvailableType** e **IMFTransform:: GetOutputAvailableType**.

O plug-in de vídeo de exemplo gerado pelo assistente de plug-in do Windows Media Player armazena a lista de formatos de vídeo com suporte como uma matriz de GUIDs. O código a seguir é do arquivo Main. cpp:


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



O player pode chamar **IMediaObject:: GetInputType** e **IMediaObject:: GetOutputType** em qualquer ordem, portanto, o código do plug-in deve prever isso. De forma semelhante, o player pode chamar **IMFTransform:: GetInputAvailableType** e **IMFTransform:: GetOutputAvailableType** em qualquer ordem. As implementações de exemplo de **GetOutputType** e **GetOutputAvailableType** testam se o tipo de entrada já foi definido. Se tiver, o plug-in responderá que ele dá suporte apenas a esse tipo. Caso contrário, o plug-in retorna o tipo que corresponde ao índice fornecido, como demonstra o código a seguir:


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>Definindo os tipos de entrada e saída

Se o plug-in do DSP estiver agindo como DMO, o Windows Media Player definirá o tipo de mídia chamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**, passando para cada função um ponteiro para uma estrutura de **\_ \_ tipo de mídia DMO** que representa o tipo de mídia solicitado.

Se o plug-in do DSP estiver agindo como um MFT, o Windows Media Player definirá o tipo de mídia chamando **IMFTransform:: SetInputType** e **IMFTransform:: SetOutputType**, passando para cada função um ponteiro para uma interface **IMFMediaType** que representa o tipo de mídia solicitado.

Não há nenhuma garantia de que o Player chamará métodos de negociação de formato em qualquer ordem específica, portanto, o código de plug-in deve lidar com qualquer caso. Por exemplo, se o Player chamar **Setoutputtypetype** antes de chamar **SetInputType**, ele será um curso de ação válido para que o plug-in rejeite o tipo de mídia de saída proposto. O código a seguir da implementação de exemplo de **IMediaObject:: SetOutputType** demonstra isso:


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



As implementações de plug-in de exemplo de **SetInputType** e **setoutputtypetype** chamam a função personalizada chamada **ValidateMediaType**. Essa função de plug-in executa uma série de testes no tipo de mídia proposto projetado para garantir que o tipo de mídia seja bem formado e tenha suporte do plug-in. O **ValidateMediaType** executa os seguintes testes:

-   Verifica se os membros **majortype** e **formatType** contêm os valores corretos.
-   Verifica se o membro do **subtipo** corresponde a um dos formatos com suporte.
-   Verifica se as informações nas estruturas **BITMAPINFOHEADER** e **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** contêm valores válidos.
-   Testa se os tipos de mídia de entrada e saída correspondem, pois o plug-in não converte formatos de entrada para saída.

Se o tipo de mídia proposto passar os testes de validação, ele será armazenado em uma variável de membro: **m \_ mtInput** para o tipo de mídia de entrada, **m \_ mtOutput** para o tipo de mídia de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in de DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




