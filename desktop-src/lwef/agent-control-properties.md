---
title: Propriedades de controle do agente
description: Propriedades de controle do agente
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005077"
---
# <a name="agent-control-properties"></a>Propriedades de controle do agente

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

As propriedades a seguir são acessadas diretamente do controle do agente:

-   [**Conectado**](connected-property.md)
-   [**Nome**](name-property-a.md)
-   [**RaiseRequestErrors**](raiserequesterrors-property.md)

Além disso, alguns ambientes de programação podem atribuir propriedades adicionais em tempo de design ou em tempo de execução. Por exemplo, Visual Basic adiciona as propriedades Left, index, Tag e Top que definem o local do controle em um formulário, mesmo que o controle não apareça na página do formulário em tempo de execução.

A propriedade suspensa ainda tem suporte para compatibilidade com versões anteriores, mas sempre retorna **false** porque o servidor não dá mais suporte a um estado suspenso.

 

 




