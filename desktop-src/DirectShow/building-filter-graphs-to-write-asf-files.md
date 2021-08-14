---
description: Criando grafos de filtro para gravar arquivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Criando grafos de filtro para gravar arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe53dcee310be34c321dfc2e988807184735a24b0793d68e3ca7dea10d0b29e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662736"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Criando grafos de filtro para gravar arquivos ASF

Ao criar Windows conteúdo baseado em mídia, os aplicativos normalmente usam um dos seguintes cenários:

-   Convertendo ou transcodificando conteúdo de algum outro formato em Windows Formato de Mídia.
-   Inserir conteúdo que não é Windows baseado em mídia (formatos de fluxo nativo) em arquivos ASF.
-   Capturando dados dinâmicos e codificando-os imediatamente Windows Formato de Mídia.

Transcodificação de arquivos ASF

Você pode criar um grafo de filtro de transcodificação de arquivo usando o [Wm ASF Writer](wm-asf-writer-filter.md) de várias maneiras. A maneira mais fácil é adicionar o Wm ASF Writer ao grafo de filtro e, em seguida, usar o método IGraphBuilder::RenderFile para criar o grafo automaticamente.

Uma maneira alternativa é adicionar cada filtro manualmente ao grafo e conectar os pinos. Depois de adicionar o Wm ASF Writer, configure-o usando os métodos IConfigAsfWriter se o perfil padrão não for adequado e conecte os pinos de entrada do Wm ASF Writer aos pinos de saída correspondentes nos filtros upstream.

A ilustração a seguir mostra configurações típicas de grafo de filtro de transcodificação do Wm ASF Writer.

![grafo de filtro de transcodificação](images/asf-transcode.png)

Inserindo formatos de fluxo nativo em arquivos ASF

Por padrão, o filtro Wm ASF Writer espera fluxos de áudio e vídeo descompactados em seus pinos de entrada e usa os codecs de Áudio de Mídia do Windows e vídeo de mídia do Windows para compactar os fluxos. No entanto, o contêiner de arquivo ASF pode ser usado para qualquer tipo de dados. Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como DRM (gerenciamento de direitos digitais) e metadados, sem precisar transcodificar seu conteúdo.

Para criar um arquivo ASF que contém conteúdo que não é baseado em Windows mídia, o aplicativo deve compactar o fluxo no upstream do grafo de filtro do Wm ASF Writer e ignorar o mecanismo de compactação do Wm ASF Writer chamando [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) da seguinte forma:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Em seguida, configure o filtro com o perfil desejado. É essencial que o tipo de mídia do fluxo de entrada corresponde exatamente ao formato no perfil. Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para corresponder a ele.

Ao conectar o Wm ASF Writer ao filtro upstream, use o método IGraphBuilder::ConnectDirect. Não use nenhum método de "conexão inteligente", como IGraphBuilder::Conexão ou IGraphBuilder::RenderFile para conectar o filtro, pois isso desabilitará o modo de "ignorar compactação" do filtro.

Capturando diretamente de um dispositivo para um arquivo ASF

Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro será semelhante ao seguinte, dependendo do tipo de dispositivo de captura que está sendo usado.

![gráfico de captura de vídeo de mídia do Windows](images/asf-webcam.png)

Para obter mais informações sobre como criar gráficos de captura de áudio e vídeo, consulte os seguintes tópicos:

-   [Captura de áudio](audio-capture.md)
-   [Captura de vídeo](video-capture.md)

O Wm ASF Writer não será executado, a menos que todos os seus pinos sejam conectados. Se você configurar o Wm ASF Writer com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um pino de entrada para cada fluxo e cada um desses pinos deverá estar conectado. Se você não pretende capturar áudio, por exemplo, configure o filtro com um perfil somente vídeo para que nenhum pino de áudio seja criado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



