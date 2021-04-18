---
title: Monitorando o progresso de compactadores e descompactadores
description: Monitorando o progresso de compactadores e descompactadores
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- VCM (Gerenciador de compactação de vídeo), monitoramento
- VCM (Gerenciador de compactação de vídeo), monitoramento
- Função ICSetStatusProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760412"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Monitorando o progresso de compactadores e descompactadores

Seu aplicativo pode monitorar o progresso de uma operação demorada executada por um compactador ou descompactador enviando-lhe o endereço de uma função de retorno de chamada. Você pode usar a função [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para enviar o endereço para o compactador ou descompactador. Quando o compactador ou o descompactador recebe esse endereço, ele envia mensagens de status para a função. Essas mensagens indicam se a operação está iniciando, parando, gerando ou continuando.

 

 




