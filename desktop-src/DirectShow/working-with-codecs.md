---
description: Trabalhando com codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Trabalhando com codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764705"
---
# <a name="working-with-codecs"></a>Trabalhando com codecs

O Microsoft Windows fornece vários codecs como componentes do sistema operacional. Os codecs disponíveis sempre incluem aqueles fornecidos com qualquer versão do DirectX e do Windows Media Player incluídos na versão do Windows. Codecs adicionais podem ser instalados quando versões mais recentes do DirectX ou do Windows Media Player ou os tempos de execução do SDK do Windows Media são instalados. Terceiros podem instalar codecs adicionais em um sistema de host; esses codecs podem ser projetados para funcionar apenas com um aplicativo específico ou podem dar suporte ao uso geral por qualquer aplicativo do DirectShow.

Os codecs podem ser implementados de uma das três maneiras diferentes:

-   Como um vídeo para o codec instalável por áudio do tipo Windows ou vídeo que é carregado pelo VCM (Gerenciador de compactação de vídeo) ou o ACM (Gerenciador de compactação de áudio). Em geral, essa tecnologia é considerada preterida e seu uso não é recomendado. Os codecs instaláveis participam de gráficos de filtro do DirectShow por meio do filtro de wrapper do descompactador AVI.
-   Como um filtro do DirectShow. Muitos codecs de terceiros são implementados como filtros nativos do DirectShow. Um desses filtros é o filtro de descompactação de MP3 Frauenhofer. Em geral, esses filtros podem ser adicionados ao grafo de filtro de maneira usual. Uma exceção a essa regra é que alguns codecs de vídeo do Windows Media™ ou Windows Media, e o codec Microsoft MPEG-4, não podem ser adicionados manualmente a um grafo de filtro. Esses filtros só podem ser adicionados pelos filtros leitor de ASF e gravador ASF.
-   Como DMOs (objetos de mídia do DirectX). DMOs são a maneira recomendada de implementar codecs, pois eles podem ser usados dentro de um grafo de filtro do DirectShow usando o filtro de invólucro do DMO ou, independentemente, em qualquer outro aplicativo de streaming baseado em DirectShow. Alguns codecs de vídeo de áudio do Windows e Windows Media são implementados como DMOs. Assim como nos filtros de mídia do Windows, esses DMOs não podem ser usados fora do contexto do SDK do Windows Media. Isso significa que, no DirectShow, eles só podem ser adicionados a um grafo por meio dos filtros do leitor ASF ou do gravador ASF.

No GraphEdit, todos esses tipos diferentes de codecs aparecem juntos nas seguintes categorias:

-   Compactador de áudio
-   Compressor de vídeo
-   Filtro do DirectShow

Muitos desses codecs, no entanto, são instalados por terceiros ou por outros aplicativos da Microsoft ou componentes do sistema operacional, e não são destinados ao uso por outros aplicativos do DirectShow. A lista de codecs visíveis no GraphEdit também depende de qual versão do Windows está sendo executada no sistema host e qual versão do SDK do DirectShow está instalada.

 

 



