---
description: Saiba como criar um manipulador de propriedades que lê e grava propriedades de e para um fluxo de arquivos. Cada manipulador está associado a um determinado tipo de arquivo.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989261"
---
# <a name="implementing-property-handlers"></a>Implementando manipuladores de propriedade

No Windows Vista e posterior, os metadados se tornaram centrais como um método de organização de itens, como arquivos, email ou contatos. Para habilitar um sistema em que os itens podem ser pesquisados com base em seus metadados e em que os usuários podem ler ou gravar esses metadados, o Windows Vista introduziu um novo sistema de propriedades. Os metadados nesse sistema são representados por um conjunto extensível de propriedades. Neste conjunto de tópicos, descrevemos como você pode criar um manipulador que lê e grava propriedades de e para um fluxo de arquivos. Esses manipuladores são chamados de manipuladores de propriedade e cada um deles é associado a determinados tipos de arquivo, identificados pela extensão de nome de arquivo.

Os tópicos a seguir discutem os requisitos e estratégias envolvidos na definição de suas propriedades e manipuladores de propriedades.

-   [Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
-   [Usando nomes de tipo](./building-property-handlers-user-friendly-kind-names.md)
-   [Usando listas de propriedades](./building-property-handlers-property-lists.md)
-   [Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md)
-   [Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
-   [Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando propriedades personalizadas](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descrição da propriedade](./propdesc-schema-entry.md)
</dt> </dl>

 

 
