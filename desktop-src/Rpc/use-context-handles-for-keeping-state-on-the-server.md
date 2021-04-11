---
title: Usar identificadores de contexto para manter o estado no servidor
description: Usar identificadores de contexto para manter o estado no servidor
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159872"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Usar identificadores de contexto para manter o estado no servidor

**Prática recomendada:** Sempre que o estado for mantido no servidor entre as chamadas, use identificadores de contexto.

Os identificadores de contexto são geralmente intimidadores para novos programadores de RPC, e a sobrecarga dos identificadores de contexto de aprendizado pode não parecer ser o esforço inicialmente. Vale a pena que os identificadores de contexto tenham soluções internas para muitas armadilhas comuns encontradas na programação de rede que, de outra forma, teriam de ser implementadas do zero. Entender os indicadores de contexto paga dividendos mais tarde.

 

 




