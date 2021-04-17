---
description: 'WS-Discovery define o endereçamento lógico usando URIs com base no formato urn: UUID:.'
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Usando endereços lógicos e físicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763055"
---
# <a name="using-logical-and-physical-addresses"></a>Usando endereços lógicos e físicos

O [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) define o endereçamento lógico usando URIs com base no `urn:uuid:` formato. A finalidade desse esquema de endereçamento é diferenciar a identidade do dispositivo de seu endereço IP atual. Basicamente, esse esquema fornece a funcionalidade de nomes DNS sem a necessidade de um servidor de nomes. O [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) recomenda que os dispositivos usem esse esquema de endereçamento.

O DPWS também recomenda que os serviços usem endereços físicos (também chamados de transporte). Isso permite que os clientes que não dão suporte nativo WS-Discovery mecanismos de endereçamento se comuniquem com os serviços do DPWS. Além disso, cada serviço pode definir seus endereços, o que permite o endereçamento de nível de transporte para implementações de dispositivo que gerenciam a expedição de serviço em uma camada inferior. Por fim, o uso de endereços físicos maximiza a interoperabilidade.

A desvantagem do endereçamento físico é que ele adiciona complexidade a implementações de dispositivo, pois o IP atual ou o endereço de transporte deve ser acompanhado e os metadados do dispositivo devem ser modificados de acordo. Por esse motivo, o DPWS não exige que os serviços usem endereços de transporte.

Se forem usados endereços lógicos, haverá alguns cenários em que o comportamento de implementação é indefinido. A especificação de WS-Discovery não descreve o que significa para um serviço residir em um endereço lógico. R1001 da especificação de WS-Discovery recomenda o uso de WS-Discovery em serviços hospedados por causa da informativa da rede associada.

Não é recomendável que os serviços residam em endereços lógicos, pois isso reduz a interoperabilidade. Se uma implementação absolutamente precisar residir em um endereço lógico, o serviço deverá usar o mesmo endereço lógico que o dispositivo. Se isso adicionar muita complexidade ao modelo de expedição no dispositivo, a solução recomendada será usar parâmetros de referência para diferenciar os serviços. O WSDAPI enviará mensagens para os serviços corretamente se usarem o mesmo endereço de ponto de extremidade que o dispositivo.

 

 



