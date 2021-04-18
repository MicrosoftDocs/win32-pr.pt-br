---
description: Os três tipos de namespaces no SPI do Windows Sockets (Winsock) incluem namespaces dinâmicos, estáticos e persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de namespaces no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810647"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipos de namespaces no SPI

Há três tipos diferentes de namespaces nos quais um serviço pode ser registrado:

-   Dinâmico
-   Estático
-   Persistente

Os namespaces dinâmicos permitem que os serviços se registrem com o namespace imediatamente e para que os clientes descubram os serviços disponíveis em tempo de execução. Os namespaces dinâmicos frequentemente dependem de difusões para indicar a disponibilidade contínua de um serviço de rede. Exemplos de namespaces dinâmicos incluem o namespace SAP usado em um ambiente NetWare e o namespace NBP usado pelo AppleTalk.

Os namespaces estáticos exigem que todos os serviços sejam registrados antecipadamente, ou seja, quando o namespace é criado. O DNS é um exemplo de um namespace estático. Embora haja uma maneira programática de resolver nomes, não há uma maneira programática de registrar nomes.

Namespaces persistentes permitem que os serviços se registrem com o namespace em tempo real. Ao contrário dos namespaces dinâmicos, no entanto, os namespaces persistentes retêm as informações de registro no armazenamento não volátil onde permanecem até o momento em que as solicitações de serviço são removidas. Os namespaces persistentes são Typified por serviços de diretório, como X. 500 e o NDS (serviço de diretório do NetWare). Esses ambientes permitem a adição, exclusão e modificação de propriedades de serviço. Além disso, o objeto de serviço que representa o serviço no serviço de diretório pode ter uma variedade de atributos associados ao serviço. O atributo mais importante para aplicativos cliente são as informações de endereçamento do serviço.

 

 



