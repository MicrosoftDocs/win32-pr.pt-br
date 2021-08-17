---
title: Estilos de serialização
description: Há três estilos que você pode usar para manipular os alças de serialização.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925382"
---
# <a name="serialization-styles"></a>Estilos de serialização

Há três estilos que você pode usar para manipular os alças de serialização. Eles são:

-   [Serialização de buffer fixa](fixed-buffer-serialization.md)
-   [Serialização de buffer dinâmico](dynamic-buffer-serialization.md)
-   [Serialização incremental](incremental-serialization.md)

Independentemente do estilo usado, você deve criar um alça de serialização, serializar os dados e, em seguida, liberar o alça. O estilo é definido quando o programa cria o alça e define a maneira como um buffer é manipulado. O handle mantém o contexto apropriado associado a cada um dos três estilos de serialização.

 

 




