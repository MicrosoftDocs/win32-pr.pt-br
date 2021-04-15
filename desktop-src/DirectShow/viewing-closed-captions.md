---
description: Exibindo legendas ocultas
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Exibindo legendas ocultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562614"
---
# <a name="viewing-closed-captions"></a>Exibindo legendas ocultas

Para dar suporte a legendas codificadas na televisão analógica, o filtro de captura expõe um PIN que fornece dados de VBI ou de legenda oculta. O PIN terá uma das seguintes categorias de PIN:

-   VBI PIN (fixar \_ categoria \_ VBI). Fornece um fluxo de exemplos de formato de onda VBI. Eles são passados para um filtro de decodificador que extrai os dados de legenda codificada.
-   PIN CC (fixar \_ categoria \_ CC). Entrega pares de bytes de legenda fechada, extraídos dos dados de linha-21.
-   PIN do CC de fatia de hardware ( \_ captura de vídeo CC do PINNAME \_ \_ ).

Para visualizar legendas ocultas, chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com a categoria VBI PIN e, se isso falhar, chame-a novamente com a categoria CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



O diagrama a seguir mostra um grafo de filtro típico para exibir legendas ocultas.

![Grafo de visualização de legendagem oculta](images/vidcap08.png)

Este grafo usa os seguintes filtros para exibição de legenda oculta:

-   [Conversor de t/coletor de alto-para-coletor](tee-sink-to-sink-converter.md). Aceita as informações de VBI do filtro de captura e divide-as em fluxos separados para cada um dos serviços de dados presentes no sinal. A Microsoft fornece codecs VBI para legendas codificadas, NABTS e teletextos padrão mundiais (WST).
-   [Decodificador CC](cc-decoder-filter.md). Decodifica os dados do CC das amostras de onda de VBI amostradas fornecidas pelo filtro de captura.
-   [Decodificador de linha 21](line-21-decoder-filter.md). Traduz os pares de bytes de CC e desenha o texto da legenda em bitmaps. O filtro downstream (nesse caso, o mixer de sobreposição) sobrepõe os bitmaps no vídeo.

O método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do construtor do grafo de captura adiciona esses filtros automaticamente. Se o filtro de captura tiver um PIN de CC em vez de um PIN de VBI, o PIN de CC será conectado diretamente ao filtro de decodificador de linha 21.

> [!Note]  
> Se você estiver usando o filtro de processador de mixagem de vídeo (VMR) para renderização, use o filtro de decodificador de linha 21 2. Esse filtro tem a mesma funcionalidade que o decodificador de linha 21, mas o CLSID é CLSID \_ Line21Decoder2.

 

> [!Note]  
> O filtro de decodificador de CC foi removido do Windows Vista. Os novos aplicativos devem usar o filtro VBICodec, documentado na documentação das tecnologias de TV da Microsoft.

 

Se o dispositivo de captura usar uma porta de vídeo, o filtro de captura poderá ter uma porta de vídeo VBI PIN (PIN \_ Category \_ VIDEOPORT \_ VBI). Esse PIN deve ser conectado ao filtro de [alocador de superfície VBI](vbi-surface-allocator.md) , que aloca superfícies para manter os dados VBI capturados. O método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adicionará esse filtro se for necessário. O diagrama a seguir mostra um gráfico de filtro com o alocador de superfície VBI.

![Grafo de visualização de legenda codificada com alocador de superfície VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Habilitando e desabilitando as legendas

Para controlar a exibição de legendas, use a interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) no filtro linha 21 de decodificador. Por exemplo, você pode desativar a exibição de legendas usando o método [**IAMLine21Decoder:: Setservicestate**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , da seguinte maneira:


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



Este exemplo usa o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para localizar a interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) . O primeiro parâmetro para **FindInterface** é **&parecer \_ \_ somente DOWNSTREAM**, que especifica a pesquisa downstream do filtro de captura (*pcap*).

### <a name="capturing-closed-caption-bitmaps"></a>Capturando bitmaps de legenda oculta

Você pode capturar os bitmaps de legenda em um arquivo. Para fazer isso, adicione a seção de gravação de arquivo do gráfico de filtro, conforme descrito em [capturando vídeo em um arquivo](capturing-video-to-a-file.md). Em seguida, processe o PIN CC ou VBI para o filtro Mux:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Se você também estiver capturando o vídeo, isso criará um arquivo com dois fluxos de vídeo separados. Ele não capturará vídeo com legendas sobrepostas sobre a imagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Legendas e teletextos codificados](closed-captions-and-teletext.md)
</dt> </dl>

 

 



