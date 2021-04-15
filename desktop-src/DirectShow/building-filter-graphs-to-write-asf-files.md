---
description: Criando gráficos de filtro para gravar arquivos ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Criando gráficos de filtro para gravar arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456762"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Criando gráficos de filtro para gravar arquivos ASF

Ao criar conteúdo baseado no Windows Media, os aplicativos normalmente usam um dos seguintes cenários:

-   Conversão ou transcodificação de conteúdo de outro formato para o Windows Media Format.
-   Inserção de conteúdo que não é baseado no Windows Media (formatos de fluxo nativos) em arquivos ASF.
-   Capturar dados dinâmicos e codificá-los imediatamente no formato de mídia do Windows.

Transcodificação de arquivos ASF

Você pode criar um grafo de filtro de transcodificação de arquivo usando o [gravador ASF do WM](wm-asf-writer-filter.md) de várias maneiras. A maneira mais fácil é adicionar o gravador ASF do WM ao grafo de filtro e, em seguida, usar o método IGraphBuilder:: RenderFile para criar o grafo automaticamente.

Uma maneira alternativa é adicionar cada filtro manualmente ao grafo e conectar os Pins. Depois de adicionar o gravador ASF do WM, configure-o usando os métodos IConfigAsfWriter se o perfil padrão não for adequado e conecte os Pins de entrada do gravador ASF do WM aos pins de saída correspondentes nos filtros upstream.

A ilustração a seguir mostra as configurações típicas de gráfico de filtro de transcodificação do gravador ASF do WM.

![transcodificação do grafo de filtro](images/asf-transcode.png)

Inserindo formatos de fluxo nativos em arquivos ASF

Por padrão, o filtro do gravador ASF do WM espera fluxos de áudio e vídeo descompactados em seus PINs de entrada e usa os codecs de vídeo do Windows Media Audio e Windows Media para compactar os fluxos. No entanto, o contêiner do arquivo ASF pode ser usado para qualquer tipo de dados. Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como metadados e DRM (gerenciamento de direitos digitais), sem a necessidade de transcodificar o conteúdo.

Para criar um arquivo ASF que contém conteúdo que não é baseado no Windows Media, o aplicativo deve compactar o fluxo no fluxo do grafo de filtro do gravador ASF do WM e ignorar o mecanismo de compactação do gravador ASF do WM chamando [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) da seguinte maneira:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Em seguida, configure o filtro com o perfil desejado. É essencial que o tipo de mídia do fluxo de entrada corresponda exatamente ao formato no perfil. Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para fazer a correspondência.

Ao conectar o gravador ASF do WM ao filtro upstream, use o método IGraphBuilder:: ConnectDirect. Não use nenhum método de "conexão inteligente" como IGraphBuilder:: Connect ou IGraphBuilder:: RenderFile para conectar o filtro, pois isso desabilitará o modo "ignorar compactação" do filtro.

Capturando diretamente de um dispositivo para um arquivo ASF

Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro será semelhante ao seguinte, dependendo do tipo de dispositivo de captura que está sendo usado.

![Grafo de captura de vídeo do Windows Media](images/asf-webcam.png)

Para obter mais informações sobre como criar gráficos de captura de áudio e vídeo, consulte os seguintes tópicos:

-   [Captura de áudio](audio-capture.md)
-   [Captura de vídeo](video-capture.md)

O gravador ASF do WM não será executado, a menos que todos os seus PINs estejam conectados. Se você configurar o gravador ASF do WM com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um PIN de entrada para cada fluxo e cada um desses Pins deverá ser conectado. Se você não pretende capturar áudio, por exemplo, certifique-se de configurar o filtro com um perfil somente de vídeo para que nenhum PIN de áudio seja criado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



