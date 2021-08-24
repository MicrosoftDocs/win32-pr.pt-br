---
description: Disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Projetando para disponibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f248b9ac9ed91788713e7ef02b4e7da0a2d7eb0c2070b1240e07dbce21b5895c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637656"
---
# <a name="designing-for-availability"></a>Projetando para disponibilidade

Disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor. Isso significa que o cliente continua a ser atendido por meio da falha e que, idealmente, a falha é transparente para o cliente. Obviamente, a falha pode vir de fontes de hardware ou software, portanto, você deve desenvolver para ambos os casos.

A disponibilidade pode ser afetada pelos seguintes fatores:

-   Modelo de aplicativo. Para maior disponibilidade, verifique se a lógica crítica do aplicativo é realizada usando o [serviço de transações COM+.](com--transactions.md) Além disso, o uso de um mecanismo de compensação pode ser eficaz para garantir que os recursos permaneçam em um estado íntegre após falhas.
-   Modelo de cliente. Integre a lógica de "tentar novamente em caso de falha" no aplicativo cliente e busque uma degradação normalmente no aplicativo se os recursos ou serviços não estão disponíveis. Entenda o que o cliente está esperando do aplicativo e crie um design que permita alternativas quando ocorrer uma falha.
-   Disponibilidade de dados/estado. Para acesso consistente a dados persistentes, use Windows Clustering para fornecer suporte a failover.
-   Disponibilidade do serviço. Você pode usar o Balanceamento de Carga de Rede para balancear a carga das solicitações de IP de entrada em um cluster de servidores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando para implantação](designing-for-deployment.md)
</dt> <dt>

[Projetando para escalabilidade](designing-for-scalability.md)
</dt> <dt>

[Projetando para segurança](designing-for-security.md)
</dt> </dl>

 

 



