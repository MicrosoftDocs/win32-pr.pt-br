---
title: Rotas e a melhor rota
description: Uma rota é um caminho de rede \ 0034; \ 0034; para um destino que tem um determinado custo associado a ele. O custo é representado por sua preferência administrativa e sua métrica específica de protocolo. As rotas com custos mais baixos são preferenciais em todas as outras rotas.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105775656"
---
# <a name="routes-and-the-best-route"></a>Rotas e a melhor rota

Uma rota é um "caminho de rede" para um destino que tem um determinado custo associado a ele. O custo é representado por sua preferência administrativa e sua métrica específica de protocolo. As rotas com custos mais baixos são preferenciais em todas as outras rotas.

Uma entrada de rota na tabela de roteamento inclui:

-   Um identificador para o destino
-   O proprietário desta rota
-   O vizinho (par) que forneceu as informações de rota
-   Sinalizadores associados ao estado da rota
-   Sinalizadores associados à rota
-   A preferência e a métrica para a rota
-   A lista de exibições às quais a rota pertence
-   Informações que são privadas para o proprietário da rota
-   Uma lista de próximos saltos usados para alcançar o destino

Os valores a seguir, em conjunto, identificam exclusivamente uma rota na tabela de roteamento:

-   A rede de destino
-   O proprietário da rota
-   O vizinho que forneceu a rota

## <a name="metrics-and-preference"></a>Métricas e preferência

Cada rota tem uma preferência administrativa (especificada pela política de roteamento) e uma métrica dependente do cliente. O Gerenciador de tabela de roteamento usa essas informações para determinar qual rota é a melhor rota para um destino. Rotas com preferência mais baixa são rotas melhores (uma sendo a mais baixa e, portanto, melhor). Se duas rotas tiverem a mesma preferência, a rota com a métrica mais baixa será a melhor rota.

Normalmente, a preferência de uma rota é determinada pela preferência do cliente que adicionou a rota. No entanto, para todas as rotas adicionadas usando a ferramenta de gerenciamento de Netsh.exe, um valor de preferência pode ser especificado por rota.

A preferência é normalmente usada para indicar a prioridade entre os clientes. Por exemplo, um administrador pode atribuir ao OSPF uma preferência mais baixa (melhor) do que o RIP. Nesse caso, as rotas OSPF são preferíveis para rotas RIP.

 

 




