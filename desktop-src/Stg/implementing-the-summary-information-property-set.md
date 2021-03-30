---
title: Implementando o conjunto de propriedades de informações de resumo
description: Há diretrizes a serem seguidas ao implementar um conjunto de propriedades de informações resumidas para o armazenamento estruturado.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementando o conjunto de propriedades de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634835"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementando o conjunto de propriedades de informações de resumo

Há diretrizes a serem seguidas ao implementar um conjunto de propriedades de informações resumidas para o armazenamento estruturado.

Veja a seguir as diretrizes para implementar [o conjunto de propriedades Resumo de informações](the-summary-information-property-set.md):

-   **Pid \_ MODELO** refere-se a um documento externo contendo informações de formato e estilo. O processo pelo qual o modelo está localizado é definido pela implementação.
-   **Pid \_ LASTAUTHOR** é o nome armazenado nas informações do usuário pelo aplicativo. Por exemplo, Mary cria um documento em seu computador e o fornece a João, que, em seguida, modifica e salva. Mary é o autor, João é o último salvo por valor.
-   **Pid \_ REVNUMBER** é o número de vezes que o comando arquivo/salvar foi chamado neste documento.
-   Cada um dos valores de data/hora deve ser armazenado em UTC (horário coordenado universal).
-   **Pid \_ CREATE \_ DTM** é uma propriedade somente leitura; Essa propriedade deve ser definida quando um documento é criado, mas não deve ser alterada posteriormente.
-   Para **a \_ miniatura de PID**, os aplicativos devem armazenar dados no formato de **\_ METAFILEPICT** do CF **ou do CF \_** . **CF \_ METAFILEPICT** é recomendado.
-   **Pid \_ SEGURANÇA** é o nível de segurança sugerido para o documento. Ao observar o nível de segurança no documento, um aplicativo que não seja o originador do documento pode ajustar sua interface do usuário para as propriedades. Um aplicativo não deve exibir nenhuma informação sobre um documento protegido por senha ou habilitar modificações em documentos Read-Only ou bloqueados para anotações em vigor. Se o usuário tentar modificar as propriedades, o aplicativo deverá avisar o usuário sobre o status de Read-Only recomendado.



| Nível de segurança         | Valor |
|------------------------|-------|
| Nenhum                   | 0     |
| Protegido por senha     | 1     |
| Somente leitura recomendado  | 2     |
| Imposto somente leitura     | 4     |
| Bloqueado para anotações | 8     |



 

 

 




