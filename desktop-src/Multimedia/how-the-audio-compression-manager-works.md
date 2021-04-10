---
title: Como funciona o Gerenciador de compactação de áudio
description: Como funciona o Gerenciador de compactação de áudio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- áudio de multimídia, Gerenciador de compactação de áudio (ACM)
- áudio, Gerenciador de compactação de áudio (ACM)
- Gerenciador de compactação de áudio (ACM), sobre
- ACM (Gerenciador de compactação de áudio), sobre
- Gerenciador de compactação de áudio (ACM), drivers de codec
- ACM (Gerenciador de compactação de áudio), drivers de codec
- Gerenciador de compactação de áudio (ACM), drivers de conversor de formato
- ACM (Gerenciador de compactação de áudio), drivers de conversor de formato
- Gerenciador de compactação de áudio (ACM), filtrar drivers
- ACM (Gerenciador de compactação de áudio), drivers de filtro
- Gerenciador de compactação de áudio (ACM), drivers de compressor
- ACM (Gerenciador de compactação de áudio), drivers de compressor
- Gerenciador de compactação de áudio (ACM), drivers de descompactação
- ACM (Gerenciador de compactação de áudio), drivers de descompactação
- drivers de codec
- drivers do conversor de formato
- drivers de filtro
- drivers de compressor
- drivers de descompactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292339"
---
# <a name="how-the-audio-compression-manager-works"></a>Como funciona o Gerenciador de compactação de áudio

O ACM usa ganchos de interface de driver existentes para substituir o algoritmo de mapeamento padrão para dispositivos de formato de onda-áudio. Isso permite que o ACM intercepte chamadas de abertura de dispositivos. Depois que uma chamada foi interceptada, o ACM pode executar uma variedade de tarefas para processar os dados de áudio, como inserir um compressor externo ou descompactar na sequência.

O ACM gerencia os seguintes tipos de drivers:

-   Drivers de compactador e descompactador (codec)
-   Drivers do conversor de formato
-   Drivers de filtro

Os compactadores e os descompactadores alteram um tipo de formato para outro. Por exemplo, um compressor ou descompactador pode alterar um arquivo de PCM (modulação de código de pulso) para um arquivo de ADPCM (modulação diferencial de código de pulso). Os conversores de formato alteram o formato, mas não o tipo de dados. Por exemplo, um conversor pode alterar 44-kHz, dados de 16 bits para 44-kHz, dados de 8 bits. Os filtros não alteram o formato de dados, mas eles alteram os dados de Wave-audio de alguma maneira. Por exemplo, um filtro pode combinar um fluxo de dados e um eco de si mesmo. Um único driver do ACM ou uma marca de filtro ou de formato em um driver pode também dar suporte a combinações dos tipos anteriores.

Para saída de Wave-Audio, o ACM passa cada buffer de dados para o conversor conforme ele chega. O conversor descompacta os dados e retorna os dados descompactados para o ACM em um buffer de "sombra". Em seguida, o ACM passa o buffer de sombra descompactado para o driver de áudio de onda. O ACM aloca os buffers de sombra sempre que recebe uma mensagem de preparação.

Para entrada de formato de onda-áudio, o ACM transmite buffers de sombra vazios para o driver. Ele usa uma tarefa em segundo plano para receber uma notificação depois que o driver preencher o buffer de sombra. Em seguida, o ACM passa os buffers para o driver para a compactação. Após a conclusão da compactação, o driver passa os dados para o aplicativo.

 

 




