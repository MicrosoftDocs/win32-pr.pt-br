---
description: Exibindo legendas fechadas
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Exibindo legendas fechadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903418"
---
# <a name="viewing-closed-captions"></a>Exibindo legendas fechadas

Para dar suporte a legendas fechadas na tv anapáloga, o filtro de captura expõe um pino que fornece dados de VBI ou legenda fechada. O pino terá uma das seguintes categorias de pino:

-   Pin da VBI (PIN \_ CATEGORY \_ VBI). Fornece um fluxo de amostras de forma de onda da VBI. Eles são passados para um filtro de decodificador que extrai os dados de legenda fechado.
-   Pino CC (PIN \_ CATEGORIA \_ CC). Fornece pares de byte de legenda fechada, extraídos dos dados de linha 21.
-   Pino CC de fatia de hardware (PINNAME \_ VIDEO \_ CC \_ CAPTURE).

Para visualizar legendas fechadas, chame [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com a categoria de pino da VBI e, se isso falhar, chame-a novamente com a categoria CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



O diagrama a seguir mostra um grafo de filtro típico para exibir legendas fechadas.

![gráfico de visualização de legendas fechadas](images/vidcap08.png)

Esse grafo usa os seguintes filtros para exibição de legenda fechada:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Aceita as informações da VBI do filtro de captura e as divide em fluxos separados para cada um dos serviços de dados presentes no sinal. A Microsoft fornece codecs de VBI para Legenda Fechada, NABTS e WST (World Standard Teletext).
-   [Decodificador CC](cc-decoder-filter.md). Decodifica dados cc das formações de onda de VBI amostradas fornecidas pelo filtro de captura.
-   [Decodificador de linha 21](line-21-decoder-filter.md). Converte os pares de byte CC e desenha o texto da legenda em bitmaps. O filtro downstream (nesse caso, o Mixer sobreposição) sobrepõe os bitmaps no vídeo.

O método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do Construtor Graph Capture adiciona esses filtros automaticamente. Se o filtro de captura tiver um pino CC em vez de um pino de VBI, o pino CC será conectado diretamente ao filtro de Decodificador de Linha 21.

> [!Note]  
> Se você estiver usando o filtro VMR (Video Mixing Renderer) para renderização, use o Filtro de Decodificador de Linha 21. Esse filtro tem a mesma funcionalidade que o Decodificador de Linha 21, mas o CLSID é CLSID \_ Line21Decoder2.

 

> [!Note]  
> O filtro do Decodificador CC foi removido Windows Vista. Novos aplicativos devem usar o filtro VBICodec, que está documentado na documentação da Microsoft TV Technologies.

 

Se o dispositivo de captura usar uma porta de vídeo, o filtro de captura poderá ter um pino de VBI de porta de vídeo (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Esse pino deve ser conectado ao filtro alocador de superfície da [VBI,](vbi-surface-allocator.md) que aloca superfícies para manter os dados de VBI capturados. O [**método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adiciona esse filtro se for necessário. O diagrama a seguir mostra um grafo de filtro com o Alocador de Superfície de VBI.

![grafo de visualização de legenda fechada com alocador de superfície de vbi](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Habilitando e desabilitando as legendas

Para controlar a exibição de legenda, use a interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) no filtro Decodificador de Linha 21. Por exemplo, você pode desativar a exibição de legenda usando o [**método IAMLine21Decoder::SetServiceState,**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) da seguinte forma:


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



Este exemplo usa o [**método ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para localizar a interface [**IAMLine21Decoder.**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) O primeiro parâmetro para **FindInterface** é **&LOOK DOWNSTREAM \_ \_ ONLY**, que especifica a pesquisa downstream do filtro de captura (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Capturando bitmaps de legendas fechadas

Você pode capturar os bitmaps de legenda em um arquivo. Para fazer isso, adicione a seção de gravação de arquivo do grafo de filtro, conforme descrito em [Capturando vídeo em um arquivo](capturing-video-to-a-file.md). Em seguida, renderizar o pino CC ou VBI para o filtro mux:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Se você também estiver capturando o vídeo, isso criará um arquivo com dois fluxos de vídeo separados. Ele não capturará o vídeo com legendas sobressprovidas na parte superior da imagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Legendas fechadas e teletexto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



