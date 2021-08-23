---
title: Usar alças de contexto para manter o estado no servidor
description: Usar alças de contexto para manter o estado no servidor
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9360d4edf95c06cef30a0e07f0e541a89823e89b163d5bbb61e0fb686a4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010954"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Usar alças de contexto para manter o estado no servidor

**Melhor prática:** Sempre que o estado for mantido no servidor entre chamadas, use os alças de contexto.

Os alças de contexto geralmente são ofensivos para novos programadores RPC, e a sobrecarga dos alças de contexto de aprendizado pode inicialmente não parecer valer a pena. Vale a pena porque os alças de contexto têm soluções internas para muitas armadilhas comuns encontradas na programação de rede que, de outra forma, teriam que ser implementadas do zero. Entender os lidadores de contexto paga dividendos mais tarde.

 

 




