---
title: Tipos de identificadores de associação
description: Os identificadores de associação podem ser automáticos, implícitos ou explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005880"
---
# <a name="types-of-binding-handles"></a>Tipos de identificadores de associação

Os identificadores de associação podem ser automáticos, implícitos ou explícitos. Elas diferem na quantidade de controle que o aplicativo tem sobre o processo de ligação. Como o nome sugere, a ligação automática manipula a vinculação automatizada. Os aplicativos cliente e servidor não precisam de código para lidar com o processo de associação. Os identificadores de associação implícitas permitem que os programas cliente configurem o identificador de associação antes que a associação ocorra. Depois que o cliente estabelece uma associação, a biblioteca de tempo de execução RPC manipula o restante. Os identificadores de associação explícitos movem o controle completo sobre o processo de associação no código-fonte do cliente e nos programas do servidor. Com esse controle vem maior complexidade. Seu aplicativo deve chamar funções RPC para gerenciar a associação. Isso não acontece automaticamente. Identificadores de associação explícitos são recomendados.

O diagrama a seguir ilustra as diferenças entre identificadores de associação automáticos, implícitos e explícitos.

![diferenças entre identificadores de associação automático, implícito e explícito](images/bhand.png)

Além disso, cada identificador de associação é primitivo ou personalizado. Cada tipo de identificador de associação é discutido nos seguintes tópicos:

-   [Identificadores de associação automática](automatic-binding-handles.md)
-   [Identificadores de associação implícita](implicit-binding-handles.md)
-   [Identificadores de associação explícitos](explicit-binding-handles.md)
-   [Identificadores de associação primitivos e personalizados](primitive-and-custom-binding-handles.md)

 

 




