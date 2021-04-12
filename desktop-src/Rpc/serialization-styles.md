---
title: Estilos de serialização
description: Há três estilos que você pode usar para manipular identificadores de serialização.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364207"
---
# <a name="serialization-styles"></a>Estilos de serialização

Há três estilos que você pode usar para manipular identificadores de serialização. Eles são:

-   [Serialização de buffer fixa](fixed-buffer-serialization.md)
-   [Serialização de buffer dinâmico](dynamic-buffer-serialization.md)
-   [Serialização incremental](incremental-serialization.md)

Independentemente do estilo usado, você deve criar um identificador de serialização, serializar os dados e, em seguida, liberar o identificador. O estilo é definido quando o programa cria o identificador e define a maneira como um buffer é manipulado. O identificador mantém o contexto apropriado associado a cada um dos três estilos de serialização.

 

 




