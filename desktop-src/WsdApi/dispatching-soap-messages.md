---
description: Há muitas maneiras de lidar com a expedição de mensagens SOAP recebidas para o serviço apropriado. Os dois mecanismos mais simples são expedição no nível de transporte e expedição de endereço e ação.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Expedindo mensagens SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579c01d03a76fcadc1ee82a270c8e222cbf68aa739d10bed0749bb82bcda80ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030246"
---
# <a name="dispatching-soap-messages"></a>Expedindo mensagens SOAP

Há muitas maneiras de lidar com a expedição de mensagens SOAP recebidas para o serviço apropriado. Os dois mecanismos mais simples são expedição no nível de transporte e expedição de endereço e ação.

## <a name="transport-level-dispatch"></a>Expedição de nível de transporte

Com a expedição de nível de transporte, o servidor HTTP subjacente (como a [API HTTP](/windows/desktop/Http/http-api-start-page)) é usado para gerenciar o roteamento de solicitações para o dispositivo e seus serviços. O servidor fornece uma URL diferente para cada serviço e para o dispositivo e diferentes sinks são registrados para cada URL. Isso permite que o código seja projetado de modo que cada serviço seja isolado do outro, seja em execução como componentes separados dentro do mesmo processo ou em execução como processos separados.

A expedição no nível de transporte tem algumas vantagens. As mensagens podem ser enviadas para o componente apropriado sem primeiro analisar o envelope SOAP ou o corpo da mensagem. Além disso, o mecanismo existente para rotear mensagens fornecidas pela maioria das implementações de servidor HTTP pode ser reutilizável, o que significa que o código de expedição personalizado é desnecessário. Ele também isola o código de processamento SOAP entre serviços, o que fornece um nível de segurança, pois os serviços seguros evitam que as mensagens viagem pelo código comum.

## <a name="address-and-action-dispatch"></a>Expedição de endereço e ação

A expedição de endereço e ação depende dos headers SOAP para determinar o serviço apropriado para o qual a mensagem é enviada. Esse modelo também pode usar informações adicionais, como parâmetros de referência, para ajudar ainda mais a expedição.

Esse modelo incentiva a reutilização de código em toda uma pilha de mensagens em camadas, pois todo o código até o processador SOAP é compartilhado por todos os serviços. Além disso, endereços de transporte distintos para serviços não são necessários, o que significa que os endereços UUID podem ser usados para pontos de extremidade de serviço. A expedição de endereço e ação também se traduz mais diretamente em um modelo de programação. Os desenvolvedores podem conectar serviços e dispositivos em um único componente que gerencia o roteamento, em vez de precisar se conectar a uma camada HTTP ou criar componentes separados para cada serviço.

 

 
