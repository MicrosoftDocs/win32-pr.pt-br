---
description: Acompanhamento de recursos não alocados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Acompanhamento de recursos não alocados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb356a7e7243c7e6f856a0dfe165440ff0b909545703032a8442bbcced77649d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305236"
---
# <a name="tracking-non-allocated-resources"></a>Acompanhamento de recursos não alocados

O gerenciador do distribuidor pode acompanhar um recurso que não é inventariado, com base no conhecimento do tempo de vida do objeto. Quando um recurso rastreado não alocado é liberado, ele é destruído e, portanto, não é retornado ao inventário. Esse modo somente faixa para recursos que são baratos de criar e destruir é mais útil do que armazenar no inventário. Esse modo também é útil para gerenciar um distribuidor de memória ou para um recurso difícil de inventariar porque há muitos tipos diferentes.

No modo somente faixa, um distribuidor de recursos cria diretamente um recurso solicitado em vez de solicitar que o gerenciador de distribuidores aloce um do inventário. Antes de retornar esse recurso para o componente do aplicativo solicitante, o distribuidor de recursos informa ao gerenciador do distribuidor para acompanhar o recurso, o que garante que, mesmo que o componente não liberar o recurso, o gerenciador do distribuidor fará isso quando o tempo de vida do componente for longo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



