---
title: Controle de captura preciso
description: Controle de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funções de retorno de chamada AVICap, controle de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372652"
---
# <a name="precise-capture-control"></a>Controle de captura preciso

Uma janela de captura pode fornecer a função de retorno de chamada de controle de captura com controle preciso ao longo do tempo em que a captura de streaming começa e termina. A primeira mensagem enviada do driver de captura para o procedimento de retorno de chamada define o parâmetro *nState* para CONTROLCALLBACK \_ Prevert após a alocação de todos os buffers e todas as outras preparações de captura são concluídas. Essa mensagem fornece ao aplicativo a capacidade de fazer o registro das fontes de vídeo. (A função de retorno de chamada especifica *nState* como seu segundo parâmetro.) A função de retorno de chamada retorna na gravação exata do momento para começar. Um valor de retorno de **true** da função de retorno de chamada continua a captura. Um valor de retorno de **false** anula A captura. Depois que a captura começa, a função de retorno de chamada é chamada com frequência com *nState* definido como CONTROLCALLBACK \_ Capture para permitir que o aplicativo encerre a captura retornando **false**.

 

 




