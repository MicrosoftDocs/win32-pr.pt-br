---
description: A disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Projetando para disponibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500924"
---
# <a name="designing-for-availability"></a>Projetando para disponibilidade

A disponibilidade é a capacidade de um aplicativo tolerar falhas em recursos do servidor. Isso significa que o cliente continua a ser servido por meio da falha e isso, idealmente, a falha é transparente para o cliente. Obviamente, a falha pode vir de fontes de hardware ou software, portanto, você deve desenvolver para ambos os casos.

A disponibilidade pode ser afetada pelos seguintes fatores:

-   Modelo de aplicativo. Para maior disponibilidade, verifique se a lógica de aplicativo crítica é conduzida usando o serviço de [Transações com+](com--transactions.md) . Além disso, o uso de um mecanismo de compensação pode ser eficaz para garantir que os recursos permaneçam em um estado íntegro após falhas.
-   Modelo de cliente. Integre a lógica de "repetição em caso de falha" no aplicativo cliente e procure uma degradação normal no aplicativo se os recursos ou serviços estiverem indisponíveis. Entenda o que o cliente está esperando do aplicativo e crie um design que permita alternativas quando ocorrer uma falha.
-   Disponibilidade de dados/estado. Para ter acesso consistente a dados persistentes, use o clustering do Windows para fornecer suporte a failover.
-   Disponibilidade do serviço. Você pode usar o balanceamento de carga de rede para balancear a carga de solicitações de entrada de IP em um cluster de servidores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando para implantação](designing-for-deployment.md)
</dt> <dt>

[Projetando para escalabilidade](designing-for-scalability.md)
</dt> <dt>

[Projetando para segurança](designing-for-security.md)
</dt> </dl>

 

 



