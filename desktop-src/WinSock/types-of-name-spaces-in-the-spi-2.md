---
description: Os três tipos de namespaces na SPI Windows (Winsock) incluem namespaces dinâmicos, estáticos e persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de namespaces na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec933650825e891a723cbbc041ad4f631c6f54b7b2b4f6a255359b640509ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733186"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipos de namespaces na SPI

Há três tipos diferentes de namespaces nos quais um serviço pode ser registrado:

-   Dinâmico
-   Estático
-   Persistente

Os namespaces dinâmicos permitem que os serviços se registrem com o namespace em tempo real e que os clientes descubram os serviços disponíveis em tempo de operação. Namespaces dinâmicos frequentemente dependem de difusões para indicar a disponibilidade contínua de um serviço de rede. Exemplos de namespaces dinâmicos incluem o namespace sap usado em um ambiente netWare e o namespace NBP usado pelo AppleTalk.

Os namespaces estáticos exigem que todos os serviços sejam registrados com antecedência, ou seja, quando o namespace é criado. O DNS é um exemplo de um namespace estático. Embora haja uma maneira programática de resolver nomes, não há nenhuma maneira programática de registrar nomes.

Namespaces persistentes permitem que os serviços se registrem com o namespace em tempo real. No entanto, ao contrário dos namespaces dinâmicos, os namespaces persistentes retêm as informações de registro no armazenamento nãovolatile em que permanecem até o momento em que o serviço solicita que sejam removidos. Namespaces persistentes são tipados por serviços de diretório, como X.500 e NDS (Serviço de Diretório do NetWare). Esses ambientes permitem a adição, exclusão e modificação de propriedades de serviço. Além disso, o objeto de serviço que representa o serviço no serviço de diretório pode ter uma variedade de atributos associados ao serviço. O atributo mais importante para aplicativos cliente são as informações de endereçamento do serviço.

 

 



