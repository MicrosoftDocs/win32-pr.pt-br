---
description: Sobre os mecanismos de renderização
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Sobre os mecanismos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a398cbe342ed2e92fc23e7da034dd69cae492208e3201b3419b3999594a135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664364"
---
# <a name="about-the-render-engines"></a>Sobre os mecanismos de renderização

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

este artigo descreve como os [serviços de edição de DirectShow](directshow-editing-services.md) (DES) renderizam um projeto de edição de vídeo.

No DES, um projeto é representado como uma linha do tempo. A linha do tempo é útil porque simplifica as tarefas mais comuns na edição de vídeo, como reorganizar os clipes de origem e adicionar efeitos de vídeo. a arquitetura de fluxo de DirectShow, por outro lado, requer um grafo de filtro. Portanto, para renderizar seu projeto, você deve converter uma linha do tempo em um grafo de filtro. O componente que faz isso é chamado de *mecanismo de renderização*. o DirectShow fornece dois mecanismos de renderização:

-   Mecanismo de renderização básico: cria um grafo de filtro que fornece saída não compactada.
-   Mecanismo de processamento inteligente: compila um grafo de filtro que fornece saída compactada.

O mecanismo de processamento inteligente usa a recompactação inteligente para melhorar o desempenho. Com a recompactação inteligente, os arquivos de origem são recompactados somente quando o formato de arquivo original difere do formato de saída final. Se os formatos corresponderem, a origem nunca será descompactada. A recompactação inteligente tem suporte apenas para compactação de vídeo, não para compactação de áudio.

Para visualização, use o mecanismo de renderização básico. O mecanismo de processamento inteligente também pode visualizar, mas com menos eficiência, porque ele precisa descompactar o fluxo compactado. Para gravar arquivos, use o mecanismo de processamento inteligente se desejar a recompactação inteligente. Caso contrário, use o mecanismo de renderização básico. A recompactação inteligente pode reduzir muito o tempo necessário para gravar o arquivo.

> [!IMPORTANT]
> não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia Windows.

 

> [!IMPORTANT]
> Ambos os mecanismos de renderização criam uma janela invisível que processa as mensagens. O thread que cria o mecanismo de renderização deve ter um loop de mensagem para enviar mensagens. além disso, esse thread não deve ser encerrado até que o mecanismo de renderização e o filtro Graph Manager sejam liberados. Caso contrário, o aplicativo poderá ser bloqueado.

 

Construindo o filtro Graph

O grafo de filtro é criado em dois estágios. No primeiro estágio, o mecanismo de renderização constrói um "front-end", que é um grafo de filtro parcial. O diagrama a seguir ilustra um front-end típico:

![front-end do grafo de filtro](images/rendeng1.png)

Os subsistemas contêm vários filtros especializados, que o mecanismo de renderização monta automaticamente. O front-end contém um pino de saída para cada grupo na linha do tempo. Os Pins de saída entregam dados descompactados se você usar o mecanismo de processamento básico ou dados compactados se usar o mecanismo de processamento inteligente.

Na segunda etapa, os Pins de saída são conectados aos filtros de renderização. Para visualização, os filtros de renderização são renderizadores de vídeo e áudio. Para gravação de arquivo, os filtros de renderização são filtros multiplexadores (MUX) e filtros de gravador de arquivo.

![Concluindo o gráfico de filtro](images/rendeng2.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visualizando um Project](previewing-a-project.md)
</dt> <dt>

[gravando um Project em um arquivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



