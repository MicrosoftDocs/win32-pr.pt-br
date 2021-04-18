---
description: Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas de registro de pares \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gerenciamento de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780938"
---
# <a name="record-management"></a>Gerenciamento de registros

Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Quando os registros são criados, atualizados ou excluídos, as alterações feitas em um grafo são replicadas para todos os nós. A tabela a seguir identifica as regras para atualizar e atualizar automaticamente os registros.



| Tarefa de gerenciamento     | Regra                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atualizando um registro   | Mantenha o tempo de expiração o mesmo ou aumente. Não é possível diminuir o tempo de expiração.                                                                                                                      |
| Atualizando um registro | Use o sinalizador de [**registro de pares par \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_record) atualização automática para atualizar automaticamente um registro. Use esse sinalizador somente quando o nó que está publicando um registro estiver online. Caso contrário, não use esse sinalizador. |



 

 

 



