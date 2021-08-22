---
description: Trabalhando com codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Trabalhando com codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462a1340ef7e6a64aada586addcc73d95a993884fe2b026e74acde5fd286638c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650615"
---
# <a name="working-with-codecs"></a>Trabalhando com codecs

o Microsoft Windows fornece vários codecs como componentes do sistema operacional. os codecs disponíveis sempre incluem aqueles fornecidos com qualquer versão do DirectX e Windows Media Player foram incluídos na versão do Windows. codecs adicionais podem ser instalados quando versões mais recentes do DirectX ou Windows Media Player ou os tempos de execução do SDK do Windows Media estiverem instalados. Terceiros podem instalar codecs adicionais em um sistema de host; esses codecs podem ser projetados para funcionar apenas com um aplicativo específico ou podem dar suporte ao uso geral por qualquer aplicativo DirectShow.

Os codecs podem ser implementados de uma das três maneiras diferentes:

-   como um vídeo para o codec instalável de áudio ou vídeo do tipo Windows que é carregado pelo VCM (gerenciador de compactação de vídeo) ou do ACM (gerenciador de compactação de áudio). Em geral, essa tecnologia é considerada preterida e seu uso não é recomendado. os codecs instaláveis participam de DirectShow gráficos de filtro por meio do filtro de wrapper do descompactador AVI.
-   como um filtro de DirectShow. muitos codecs de terceiros são implementados como filtros de DirectShow nativos. Um desses filtros é o filtro de descompactação de MP3 Frauenhofer. Em geral, esses filtros podem ser adicionados ao grafo de filtro de maneira usual. uma exceção a essa regra é que alguns Windows media™ codecs de vídeo de mídia de áudio ou Windows e o codec do Microsoft MPEG-4 não podem ser adicionados manualmente a um grafo de filtro. Esses filtros só podem ser adicionados pelos filtros leitor de ASF e gravador ASF.
-   Como DMOs (objetos de mídia do DirectX). DMOs são a maneira recomendada de implementar codecs, pois eles podem ser usados dentro de um DirectShow gráfico de filtro usando o filtro de Wrapper de DMO ou, independentemente, em qualquer outro aplicativo de streaming não baseado em DirectShow. alguns codecs de vídeo de mídia de áudio e Windows de mídia Windows são implementados como DMOs. assim como ocorre com os filtros de mídia Windows, esses DMOs não podem ser usados fora do contexto do SDK de mídia do Windows. isso significa que, em DirectShow, eles só podem ser adicionados a um grafo por meio dos filtros do leitor asf ou do gravador asf.

No GraphEdit, todos esses tipos diferentes de codecs aparecem juntos nas seguintes categorias:

-   Compactador de áudio
-   Compressor de vídeo
-   filtro de DirectShow

muitos desses codecs, no entanto, são instalados por terceiros ou por outros aplicativos da Microsoft ou componentes do sistema operacional, e não são destinados ao uso por outros aplicativos DirectShow. a lista de codecs visíveis no GraphEdit também depende de qual versão do Windows está em execução no sistema host e qual versão do SDK do DirectShow está instalada.

 

 



