---
description: Antes de agosto de 2006, WS-MetadataExchange definiu seu próprio método de troca de metadados, que foi usado pelo perfil de dispositivos para serviços Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Conformidade de especificação de WS-MetadataExchange e WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091274"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Conformidade de especificação de WS-MetadataExchange e WS-Transfer

Antes de agosto de 2006, o [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) definiu seu próprio método de troca de metadados [Get](get--metadata-exchange--http-request-and-message.md) , que foi usado pelo [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). A especificação de WS-MetadataExchange versão 1,1 substituiu esse método pelo método Get definido na especificação WS-Transfer.

No modelo atual, WS-Transfer fornece o método [Get](get--metadata-exchange--http-request-and-message.md) e não faz nenhuma referência ao tipo do corpo. WS-MetadataExchange descreve o formato do corpo e um mecanismo para empacotar várias partes de metadados em uma única resposta, e DPWS descreve partes específicas de metadados que um serviço deve incluir em uma resposta de metadados.

O WSDAPI não dá suporte completo à especificação de WS-Transfer. Como apenas o método [Get](get--metadata-exchange--http-request-and-message.md) é necessário para dispositivos, nenhuma outra parte do WS-Transfer foi implementada. Além disso, o WSDAPI não implementa o método GetMetadata opcional descrito em WS-MetadataExchange.

 

 



