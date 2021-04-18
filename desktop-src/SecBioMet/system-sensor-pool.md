---
title: Pool do sensor do sistema
description: Uma coleção de unidades biométricas compartilhadas que fornecem acesso aos serviços de autenticação do Windows. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761878"
---
# <a name="system-sensor-pool"></a>Pool do sensor do sistema

O pool do sensor do sistema é uma coleção de unidades biométricas compartilhadas que fornecem acesso aos serviços de autenticação do Windows. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico. Unidades biométricas no pool do sistema:

-   Pode ser compartilhado por vários aplicativos cliente.
-   Enviar avisos de eventos gerados pela conclusão de operações biométricas somente para o aplicativo que tem o foco da janela atual.
-   Use SIDs de conta para representar as identidades do modelo. Todos os modelos associados a uma única conta de usuário são marcados com o SID atribuído a essa conta.
-   Dependa do armazenamento de modelo confiável fornecido pelo serviço biométrico do Windows.

Uma unidade biométrica pode ser incluída no pool do sistema se puder ser:

-   Configurado para operar no modo básico e agir somente como um dispositivo de captura biométrica.
-   Configurado para operar no modo avançado, mas não tem armazenamento de modelo integrado. Ou seja, ele deve usar o adaptador de armazenamento e o repositório de modelos fornecidos pela Microsoft.
-   Configurado para operar no modo avançado, contém o armazenamento de modelo integrado e pode gerar os hashes necessários.

Quando um novo dispositivo de sensor é conectado, o serviço de biometria do Windows cria uma unidade biométrica para ele e tenta configurar essa unidade para uso pelo pool do sensor do sistema. Se a configuração não for bem-sucedida, a unidade biométrica será colocada no pool de sensores não atribuído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de sensores privado](private-sensor-pool.md)
</dt> <dt>

[Pools de sensores](sensor-pools.md)
</dt> <dt>

[Comportamento do pool do sistema](system-pool-behavior.md)
</dt> </dl>

 

 




