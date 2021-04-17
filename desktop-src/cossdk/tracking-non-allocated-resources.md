---
description: Controlando recursos não alocados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Controlando recursos não alocados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765752"
---
# <a name="tracking-non-allocated-resources"></a>Controlando recursos não alocados

O Gerenciador do dispensador pode rastrear um recurso que não está inventariado, com base no conhecimento do tempo de vida do objeto. Quando um recurso rastreado não alocado é liberado, ele é destruído e, portanto, não é retornado para o inventário. Esse modo somente acompanhamento para recursos que são baratos para criar e destruir é mais útil do que armazená-los no inventário. Esse modo também é útil para gerenciar um dispensador de memória ou para um recurso que é difícil de inventariar porque há muitos tipos diferentes.

No modo somente rastreamento, um dispensador de recurso cria diretamente um recurso solicitado em vez de pedir ao Gerenciador de dispensadores para alocar um do inventário. Antes de retornar esse recurso para o componente de aplicativo solicitante, o dispensador de recursos informa o gerente do dispensador para controlar o recurso, o que garante que, mesmo que o componente fique inativo para liberar o recurso, o Gerenciador do dispensador fará isso quando o tempo de vida do componente terminar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



