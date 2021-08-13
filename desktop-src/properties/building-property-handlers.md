---
description: Saiba como criar um manipulador de propriedades que lê e grava Propriedades de e para um fluxo de arquivos. Cada manipulador está associado a um determinado tipo de arquivo.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df4012168a0b6d1af5db727907e1c0fdc07231eac42abfbd3b96e8daab2f3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469122"
---
# <a name="implementing-property-handlers"></a>Implementando manipuladores de propriedade

no Windows Vista e posterior, os metadados se tornaram centrais como um método de organizar itens, como arquivos, email ou contatos. para habilitar um sistema em que os itens podem ser pesquisados com base em seus metadados e onde os usuários podem ler ou gravar esses metadados, Windows Vista introduziu um novo sistema de propriedades. Os metadados nesse sistema são representados por um conjunto extensível de propriedades. Neste conjunto de tópicos, descrevemos como você pode criar um manipulador que lê e grava Propriedades de e para um fluxo de arquivos. Esses manipuladores são chamados de manipuladores de propriedade e cada um é associado a um determinado tipo de arquivo, identificado pela extensão de nome de arquivo.

Os tópicos a seguir abordam os requisitos e as estratégias envolvidas na definição de suas propriedades e manipuladores de propriedade.

-   [Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
-   [Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
-   [Usando listas de propriedades](./building-property-handlers-property-lists.md)
-   [Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
-   [Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
-   [Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando propriedades personalizadas](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descrição da propriedade](./propdesc-schema-entry.md)
</dt> </dl>

 

 
