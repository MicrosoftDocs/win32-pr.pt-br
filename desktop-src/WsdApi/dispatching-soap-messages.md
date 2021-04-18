---
description: Há várias maneiras de lidar com a expedição de mensagens SOAP recebidas para o serviço apropriado. Os dois mecanismos mais simples são a expedição de nível de transporte e a expedição de endereço e ação.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Expedindo mensagens SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a60e896557a64b840ec890ddc5c5d2e2cf8295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505970"
---
# <a name="dispatching-soap-messages"></a>Expedindo mensagens SOAP

Há várias maneiras de lidar com a expedição de mensagens SOAP recebidas para o serviço apropriado. Os dois mecanismos mais simples são a expedição de nível de transporte e a expedição de endereço e ação.

## <a name="transport-level-dispatch"></a>Expedição no nível de transporte

Com a expedição de nível de transporte, o servidor HTTP subjacente (como a [API http](/windows/desktop/Http/http-api-start-page)) é usado para gerenciar o roteamento de solicitações para o dispositivo e seus serviços. O servidor fornece uma URL diferente para cada serviço e para o dispositivo e coletores diferentes são registrados para cada URL. Isso permite que o código seja projetado de modo que cada serviço seja isolado do outro, seja executado como componentes separados no mesmo processo ou em execução como processos separados.

A expedição de nível de transporte tem algumas vantagens. As mensagens podem ser expedidas para o componente apropriado sem primeiro analisar o envelope SOAP ou o corpo da mensagem. Além disso, o mecanismo existente para rotear mensagens fornecidas pela maioria das implementações de servidor HTTP pode ser reutilizado, o que significa que o código de expedição personalizado é desnecessário. Ele também isola o código de processamento SOAP entre os serviços, que fornece um nível de segurança, pois os serviços seguros evitam que as mensagens percorram o código comum.

## <a name="address-and-action-dispatch"></a>Expedição de endereço e ação

A expedição de endereço e ação depende dos cabeçalhos SOAP para determinar o serviço apropriado para o qual a mensagem é expedida. Esse modelo também pode usar informações adicionais, como parâmetros de referência, para ajudar a expedição adicional.

Esse modelo incentiva a reutilização de código em uma pilha de mensagens em camadas, pois todo o código até o processador SOAP é compartilhado por todos os serviços. Além disso, endereços de transporte distintos para serviços não são necessários, o que significa que os endereços UUID podem ser usados para pontos de extremidade de serviço. A expedição de endereço e ação também se traduz mais diretamente em um modelo de programação. Os desenvolvedores podem conectar serviços e dispositivos em um único componente que gerencia o roteamento, em vez de ter que se vincular a uma camada HTTP ou criar componentes separados para cada serviço.

 

 
