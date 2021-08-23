---
title: Tipos de alças de associação
description: Os alças de associação podem ser automáticos, implícitos ou explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011065"
---
# <a name="types-of-binding-handles"></a>Tipos de alças de associação

Os alças de associação podem ser automáticos, implícitos ou explícitos. Elas diferem na quantidade de controle que o aplicativo tem sobre o processo de associação. Como o nome sugere, a associação automática lida com a automatização da associação. Os aplicativos cliente e servidor não precisam de código para lidar com o processo de associação. Os alças de associação implícita permitem que os programas cliente configurem o alça de associação antes que a associação seja realizada. Depois que o cliente estabelece uma associação, a biblioteca em tempo de executar RPC lida com o restante. Os alças de associação explícita movem o controle completo sobre o processo de associação para o código-fonte do cliente e dos programas de servidor. Com esse controle vem maior complexidade. Seu aplicativo deve chamar funções RPC para gerenciar a associação. Isso não ocorre automaticamente. Os alças de associação explícita são recomendados.

O diagrama a seguir ilustra as diferenças entre os alças de associação automática, implícita e explícita.

![diferenças entre os alças de associação automática, implícita e explícita](images/bhand.png)

Além disso, cada alça de associação é primitiva ou personalizada. Cada tipo de identificador de associação é discutido nos tópicos a seguir:

-   [Alças de associação automática](automatic-binding-handles.md)
-   [Alças de associação implícitas](implicit-binding-handles.md)
-   [Alças de associação explícitas](explicit-binding-handles.md)
-   [Alças de associação primitivas e personalizadas](primitive-and-custom-binding-handles.md)

 

 




