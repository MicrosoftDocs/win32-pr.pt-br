---
title: Fazendo e processando chamadas assíncronas
description: Objetos COM podem dar suporte à chamada assíncrona.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 173f33ea3a0d4ec59f994eeff259e776efa58ae5b0182ba97f77e1ba99dd0d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130198"
---
# <a name="making-and-processing-asynchronous-calls"></a>Fazendo e processando chamadas assíncronas

Objetos COM podem dar suporte à chamada assíncrona. Quando um cliente faz uma chamada assíncrona, o controle retorna ao cliente imediatamente. Enquanto o servidor processa a chamada, o cliente está livre para realizar outros trabalhos. Quando o cliente não puder mais continuar sem os resultados da chamada, ele poderá obter os resultados da chamada nesse momento.

Por exemplo, uma solicitação para um conjunto de registros grande ou complexo pode ser demorada. Um cliente pode solicitar o conjunto de registros por uma chamada assíncrona e, em seguida, fazer outro trabalho. Quando o conjunto de registros está disponível, o cliente pode obtê-lo rapidamente sem bloqueio.

Os clientes não fazem chamadas assíncronas diretamente no objeto de servidor. Em vez disso, eles obtêm um objeto de chamada que implementa uma versão assíncrona de uma interface síncrona no objeto Server. A interface assíncrona no objeto de chamada tem um nome do formato Async *InterfaceName*. Por exemplo, se um objeto de servidor implementar uma interface síncrona chamada IMinhaInterface, haverá um objeto de chamada que implementa uma interface assíncrona denominada AsyncIMyInterface.

> [!Note]  
> O suporte assíncrono não está disponível para **IDispatch** ou para interfaces que herdam **IDispatch**.

 

Objetos de servidor que dão suporte a chamadas assíncronas implementam a interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Essa interface expõe um único método, [**createchama**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), que cria uma instância de um objeto de chamada especificado. Os clientes podem consultar **ICallFactory** para determinar se um objeto dá suporte à chamada assíncrona.

Para cada método em uma interface síncrona, a interface assíncrona correspondente implementa dois métodos. Esses métodos anexam os prefixos Begin \_ e Finish \_ ao nome do método síncrono. Por exemplo, se uma interface chamada ISimpleStream tiver um método Read, a interface AsyncISimpleStream terá um método Begin \_ Read e Finish \_ Read. Para iniciar uma chamada assíncrona, o cliente chama o \_ método Begin.

Ao implementar um objeto de servidor, você não precisa fornecer um objeto de chamada para cada interface que o objeto implementa. Se o objeto de servidor implementar a interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) e usar o marshaling padrão, um cliente com marshaling pode sempre obter um objeto de chamada de proxy, mesmo que não haja nenhum objeto de chamada no lado do servidor. Esse proxy realizará marshaling do \_ método Begin como uma chamada síncrona, o servidor processará a chamada de forma síncrona e o cliente poderá obter os parâmetros de saída chamando o \_ método Finish.

Por outro lado, se um cliente fizer uma chamada síncrona com marshaling em uma interface para a qual há um objeto de chamada no lado do servidor, o servidor sempre processará a chamada de forma assíncrona. Esse comportamento não será aparente para o cliente, pois o cliente receberá os mesmos parâmetros de saída e o mesmo valor de retorno que ele teria recebido do método síncrono.

Em ambos os casos, a interação entre o cliente e o servidor é empacotada como se a chamada fosse síncrona: a saída de proxies síncronos e assíncronos é indistinguíveis, assim como a saída dos stubs correspondentes. Esse comportamento simplifica muito o modelo de programação tanto de clientes quanto de servidores. Se um objeto de servidor implementar [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory), um cliente com marshaling não precisa tentar criar um objeto de chamada que pode não estar disponível – para o cliente, um objeto de chamada estará sempre disponível.

Quando o cliente e o servidor estiverem no mesmo apartamento, o objeto de servidor processará qualquer chamada que o cliente fizer. Se um objeto de chamada não estiver disponível, o cliente deverá obter explicitamente a interface síncrona e fazer uma chamada síncrona.

Para obter mais informações, consulte estes tópicos:

-   [Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
-   [Cancelando uma chamada assíncrona](canceling-an-asynchronous-call.md)
-   [Cancelando chamadas de método](canceling-method-calls.md)
-   [Sincronização de chamadas](call-synchronization.md)

 

 