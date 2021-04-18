---
title: Obtendo o melhor desempenho de busca de vídeo
description: Obtendo o melhor desempenho de busca de vídeo
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- SDK do Windows Media Format, melhor desempenho de busca em vídeo
- ASF (Advanced Systems Format), melhor desempenho de busca de vídeo
- ASF (formato de sistemas avançados), melhor desempenho de busca de vídeo
- ASF (Advanced Systems Format), desempenho de busca em vídeo
- ASF (formato de sistemas avançados), desempenho de busca em vídeo
- ASF (Advanced Systems Format), desempenho
- ASF (formato de sistemas avançados), desempenho
- busca de vídeo
- desempenho, busca de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811528"
---
# <a name="getting-the-best-video-seeking-performance"></a>Obtendo o melhor desempenho de busca de vídeo

Procurar conteúdo em um arquivo é uma operação muito comum que é potencialmente um problema de desempenho. O vídeo codificado com o codec do Windows Media Video 9 é constituído principalmente por quadros Delta, que registram apenas as alterações em relação ao quadro anterior. A reconstrução de quadros Delta leva tempo, especialmente se os quadros-chave estiverem muito distantes. Para obter mais informações sobre como configurar quadros-chave para busca eficiente, consulte [Configurando fluxos de vídeo para](configuring-video-streams-for-seeking-performance.md)procurar o desempenho.

Além da configuração adequada, você pode melhorar o desempenho de busca usando a indexação de quadros para o fluxo de vídeo. A busca por um número de quadro é normalmente mais rápida do que a busca de um horário de apresentação.

Se estiver procurando em um arquivo com vários fluxos, você deverá selecionar apenas os fluxos necessários. Cada fluxo configurado para leitura afetará o desempenho da busca, porque todos os fluxos selecionados são sincronizados quando você busca um ponto em um arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para buscar por número de quadro usando o leitor assíncrono**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por número de quadro usando o leitor síncrono**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**Para procurar por tempo usando o leitor assíncrono**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por tempo usando o leitor síncrono**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




