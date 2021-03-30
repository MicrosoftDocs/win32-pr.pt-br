---
title: Independência de outros componentes
description: Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo pelo qual a cadeia passada não reconhece dados de erro estendidos ou não aproveita isso. As abordagens recomendadas para essas situações são fornecidas no final desta seção.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independência de outros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916561"
---
# <a name="independence-from-other-components"></a>Independência de outros componentes

Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo pelo qual a cadeia passada não reconhece dados de erro estendidos ou não aproveita isso. As abordagens recomendadas para essas situações são fornecidas no final desta seção.

Os dados de erro estendidos são mais úteis quando aplicativos ou servidores que usam RPC aproveitam as informações de erro estendidas. Ao investigar um \_ código de erro RPC S \_ \* e os servidores ou aplicativos envolvidos não disponibilizarem dados de erro estendidos, considere as seguintes abordagens:

-   Faça uma detecção.

    Reproduza o cenário ao fazer a detecção. A detecção da transmissão conterá os dados de erro estendidos.

-   Examine-o no depurador.

    Se um farejamento do problema não funcionar, porque a chamada é local ou porque o erro é originado localmente, anexe um depurador ao processo que retorna o erro e coloque um ponto de interrupção imediatamente após a chamada RPC gerar o erro. O RPC geralmente indica erros lançando exceções, portanto, se você estiver procurando o erro 1825 ( \_ erro de pacote RPC s s \_ \_ \_ ), habilite a exceção 1825 e quando o depurador interromper essa exceção, examine as informações de erro estendidas para o thread.

 

 




