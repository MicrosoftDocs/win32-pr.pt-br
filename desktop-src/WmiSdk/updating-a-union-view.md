---
description: Você pode atualizar os valores das propriedades não chave de instâncias de classe de exibição Union. As alterações feitas na instância da classe de exibição serão propagadas de volta para as instâncias de classe de origem que formam a classe de exibição Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Atualizando uma exibição Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091276"
---
# <a name="updating-a-union-view"></a>Atualizando uma exibição Union

Você pode atualizar os valores das propriedades não chave de instâncias de classe de exibição Union. As alterações feitas na instância da classe de exibição serão propagadas de volta para as instâncias de classe de origem que formam a classe de exibição Union.

As seguintes restrições se aplicam a alterações para exibir instâncias de classe:

-   Você não pode criar novas instâncias de classes de exibição.
-   Somente as classes Union dão suporte a atualizações; as exibições de junção e Associação criam instâncias de exibição somente leitura.
-   O sucesso de uma atualização depende se uma instância de origem é atualizável. Se uma propriedade de exibição de instância for mapeada para uma propriedade somente leitura de uma instância de origem, as tentativas de modificar a propriedade de exibição falharão.

 

 



