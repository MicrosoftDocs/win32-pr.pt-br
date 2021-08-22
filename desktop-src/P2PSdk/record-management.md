---
description: Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas DE \_ REGISTRO PAR.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gerenciamento de Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011514"
---
# <a name="record-management"></a>Gerenciamento de Registros

Para gerenciar registros, você pode trabalhar com informações armazenadas em estruturas [**DE \_ REGISTRO**](/windows/desktop/api/P2P/ns-p2p-peer_record) PAR. Quando os registros são criados, atualizados ou excluídos, as alterações feitas em um grafo são replicadas para todos os nós. A tabela a seguir identifica as regras para atualizar e atualizar automaticamente os registros.



| Tarefa de gerenciamento     | Regra                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atualizando um registro   | Mantenha o tempo de expiração igual ou aumente-o. Não é possível diminuir o tempo de expiração.                                                                                                                      |
| Atualizar um registro | Use o [**sinalizador \_ \_ \_ AUTOREFRESH DO SINALIZADOR DE**](/windows/desktop/api/P2P/ns-p2p-peer_record) REGISTRO PAR para atualizar automaticamente um registro. Use esse sinalizador somente quando o nó que está publicando um registro estiver online. Caso contrário, não use esse sinalizador. |



 

 

 



