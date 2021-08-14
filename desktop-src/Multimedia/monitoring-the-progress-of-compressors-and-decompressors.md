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
ms.openlocfilehash: 44707cb6a8fbdb19b1d71fed6c71498b51936b9d089354277c6767586b4b8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373454"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Monitorando o progresso de compactadores e descompactadores

Seu aplicativo pode monitorar o progresso de uma operação demorada executada por um compactador ou descompactador enviando-lhe o endereço de uma função de retorno de chamada. Você pode usar a função [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para enviar o endereço para o compactador ou descompactador. Quando o compactador ou o descompactador recebe esse endereço, ele envia mensagens de status para a função. Essas mensagens indicam se a operação está iniciando, parando, gerando ou continuando.

 

 




