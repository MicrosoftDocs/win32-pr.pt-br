---
title: Próximos saltos
description: As rotas têm um ou mais próximos saltos associados a elas.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004997"
---
# <a name="next-hops"></a>Próximos saltos

As rotas têm um ou mais próximos saltos associados a elas. Se o destino não estiver em uma rede conectada diretamente, o próximo salto será o endereço do próximo roteador (ou rede) na rede de saída que pode melhor rotear os dados para o destino. A melhor rota é a rota que tem o menor custo, com base na política de roteamento em uso. Cada próximo salto pode ser usado para encaminhar dados no caminho para o destino. Todas as rotas de propriedade de um cliente compartilham um conjunto comum de entradas de próximo salto que foram adicionadas pelo cliente.

Cada próximo salto é identificado exclusivamente pelo endereço do próximo salto e o índice de interface usado para alcançar o próximo salto.

Se o próximo salto em si não estiver diretamente conectado, ele será marcado como um próximo salto "remoto". Nesse caso, o encaminhador deve executar outra pesquisa usando o endereço de rede do próximo salto. Essa pesquisa é necessária para localizar o próximo salto "local" usado para alcançar o próximo salto e o destino remotos.

Uma entrada de próximo salto na tabela de roteamento inclui:

-   O endereço de rede do próximo salto
-   O proprietário do próximo salto
-   O identificador da interface de saída
-   O estado do próximo salto
-   Sinalizadores associados ao próximo salto
-   Informações que são privadas para o proprietário do próximo salto
-   Um identificador para o destino correspondente ao próximo salto remoto

 

 




