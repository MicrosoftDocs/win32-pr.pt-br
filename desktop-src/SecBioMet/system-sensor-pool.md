---
title: Pool de Sensor do Sistema
description: Uma coleção de unidades biométricas compartilháveis que fornecem acesso aos Windows de autenticação. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associe um SID a um modelo biométrico específico.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c73a187c81812355d574b6c4fb867aad8f832c504f7ec79289879565cf73bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911609"
---
# <a name="system-sensor-pool"></a>Pool de Sensor do Sistema

O pool de sensor do sistema é uma coleção de unidades biométricas compartilháveis que fornecem acesso aos Windows de autenticação. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associe um SID a um modelo biométrico específico. Unidades biométricas no pool do sistema:

-   Pode ser compartilhado por vários aplicativos cliente.
-   Envie avisos de evento gerados pela conclusão de operações biométricas somente para o aplicativo que tem o foco da janela atual.
-   Use SIDs de conta para representar as identidades de modelo. Todos os modelos associados a uma única conta de usuário são marcados com o SID atribuído a essa conta.
-   Dependa do armazenamento de modelo confiável fornecido pelo serviço Windows Biométrico.

Uma unidade biométrica poderá ser incluída no pool do sistema se puder ser:

-   Configurado para operar no modo básico e atuar apenas como um dispositivo de captura biométrica.
-   Configurado para operar no modo avançado, mas não tem armazenamento de modelo de integração. Ou seja, ele deve usar o adaptador de armazenamento e o armazenamento de modelos fornecidos pela Microsoft.
-   Configurado para operar no modo avançado, contém armazenamento de modelo de integração e pode gerar os hashes necessários.

Quando um novo dispositivo de sensor está conectado, o Windows Biométrico cria uma unidade biométrica para ele e tenta configurar essa unidade para uso pelo pool de sensor do sistema. Se a configuração não for bem-sucedida, a unidade biométrica será colocada no pool de sensor não atribuído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de Sensor Privado](private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[Comportamento do pool do sistema](system-pool-behavior.md)
</dt> </dl>

 

 




