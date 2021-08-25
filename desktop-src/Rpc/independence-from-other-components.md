---
title: Independência de outros componentes
description: Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo por meio do qual a cadeia passada não reconhece dados de erro estendidos ou não os aproveita. Abordagens recomendadas para essas situações são fornecidas no final desta seção.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independência de outros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8174ffa0469550d3a7b274fb28f2f30dd807314e6bd596b75469f717f5924a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020446"
---
# <a name="independence-from-other-components"></a>Independência de outros componentes

Os dados de erro estendidos são úteis mesmo quando o servidor ou aplicativo por meio do qual a cadeia passada não reconhece dados de erro estendidos ou não os aproveita. Abordagens recomendadas para essas situações são fornecidas no final desta seção.

Os dados de erro estendidos são mais úteis quando aplicativos ou servidores que usam RPC aproveitam as informações de erro estendidas. Ao investigar um código de erro RPC S e os servidores ou aplicativos envolvidos não disponibilizam dados de erro estendidos, considere \_ \_ \* as seguintes abordagens:

-   Dê uma farejada.

    Reproduza o cenário ao fazer a farejamento. A escuta da transmissão conterá os dados de erro estendidos.

-   Examine-o no depurador.

    Se a busca do problema não funcionar, porque a chamada é local ou porque o erro é originado localmente, anexe um depurador ao processo que retorna o erro e coloque um ponto de interrupção imediatamente após a chamada RPC gerar o erro. O RPC geralmente indica erros habilitando exceções, portanto, se você estiver procurando o erro 1825 (ERRO de PKG do RPC S SEC), habilita a exceção \_ \_ \_ 1825 e quando o depurador interrompe essa exceção, examine as informações de erro estendidas para o \_ thread.

 

 




