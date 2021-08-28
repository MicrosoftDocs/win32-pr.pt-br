---
title: Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo
description: Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- plug-ins Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, negociação de formato de vídeo
- Plug-ins do DSP, negociação de formato de vídeo
- plug-ins de DSP de vídeo, negociação de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90154f3fe7824fb9af563cb662fdcb2847339bc6061d79b3e92cab9c6e36e44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761816"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo

antes que Windows Media Player insira um plug-in de DSP de vídeo na cadeia de sinais, o Player deve determinar se o plug-in pode processar o vídeo que está sendo reproduzido. O processo pelo qual o plug-in e o Player se comunicam sobre formatos de vídeo com suporte é chamado de negociação de formato.

## <a name="providing-the-supported-input-and-output-types"></a>Fornecendo os tipos de entrada e saída com suporte

se o plug-in do DSP estiver agindo como um objeto de mídia DirectX (DMO), o Player consultará o plug-in sobre seus formatos com suporte fazendo uma sequência de chamadas para **IMediaObject:: getinputtype** e **IMediaObject:: getoutputtype**.

Se o plug-in do DSP estiver agindo como uma Media Foundation transformação (MFT), o Player consultará o plug-in sobre seus formatos com suporte fazendo uma sequência de chamadas para **IMFTransform:: GetInputAvailableType** e **IMFTransform:: GetOutputAvailableType**.

o plug-in de vídeo de exemplo gerado pelo assistente de plug-in Windows Media Player armazena a lista de formatos de vídeo com suporte como uma matriz de guids. O código a seguir é do arquivo Main. cpp:


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

se o plug-in do DSP estiver agindo como um DMO, Windows Media Player definirá o tipo de mídia chamando **IMediaObject:: setinputtype** e **IMediaObject:: setoutputtype**, passando para cada função um ponteiro para uma estrutura de **\_ \_ tipo de mídia DMO** que representa o tipo de mídia solicitado.

se o plug-in do DSP estiver agindo como um MFT, Windows Media Player definirá o tipo de mídia chamando **IMFTransform:: setinputtype** e **IMFTransform:: setoutputtype**, passando para cada função um ponteiro para uma interface **IMFMediaType** que representa o tipo de mídia solicitado.

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

 

 




