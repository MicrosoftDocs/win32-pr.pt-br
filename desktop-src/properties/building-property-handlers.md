---
description: No Windows Vista e posterior, os metadados se tornaram centrais como um método de organizar itens, como arquivos, email ou contatos.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170505"
---
# <a name="implementing-property-handlers"></a>Implementando manipuladores de propriedade

No Windows Vista e posterior, os metadados se tornaram centrais como um método de organizar itens, como arquivos, email ou contatos. Para habilitar um sistema em que os itens podem ser pesquisados com base em seus metadados e onde os usuários podem ler ou gravar esses metadados, o Windows Vista introduziu um novo sistema de propriedades. Os metadados nesse sistema são representados por um conjunto extensível de propriedades. Neste conjunto de tópicos, descrevemos como você pode criar um manipulador que lê e grava Propriedades de e para um fluxo de arquivos. Esses manipuladores são chamados de manipuladores de propriedade e cada um é associado a um determinado tipo de arquivo, identificado pela extensão de nome de arquivo.

Os tópicos a seguir abordam os requisitos e as estratégias envolvidas na definição de suas propriedades e manipuladores de propriedade.

-   [Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
-   [Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
-   [Usando listas de propriedades](./building-property-handlers-property-lists.md)
-   [Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
-   [Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
-   [Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando propriedades personalizadas](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descrição da propriedade](./propdesc-schema-entry.md)
</dt> </dl>

 

 
