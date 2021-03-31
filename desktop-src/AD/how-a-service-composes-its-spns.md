---
title: Como um serviço compõe seus SPNs
description: Um serviço pode usar duas funções para compor seus SPNs DsGetSpn é uma função de finalidade geral para compor SPNs e DsServerRegisterSpn é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome da entidade de serviço AD, como um serviço compõe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822274"
---
# <a name="how-a-service-composes-its-spns"></a>Como um serviço compõe seus SPNs

Um serviço pode usar duas funções para compor seus SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) é uma função de finalidade geral para compor SPNs e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.

Um instalador de serviço normalmente usa a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor SPNs, que, em seguida, registra na conta de logon do serviço usando a função [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) . O **DsGetSpn** pode executar as funções a seguir.

-   Crie um SPN simples com o <service class> / <host> formato "" para um serviço baseado em host.
-   Crie um SPN complexo que inclui o &lt; componente "nome do serviço &gt; " usado por serviços replicáveis ou pelo &lt; componente "porta &gt; " que distingue várias instâncias de um serviço em um único host.
-   Crie um único SPN com o &lt; componente "host &gt; " definido como o nome de um host especificado ou o nome do computador local por padrão.
-   Crie uma matriz de SPNs para várias instâncias de serviço que serão executadas em vários hosts em toda a floresta. Cada SPN especifica o nome do host para uma instância de serviço.
-   Crie uma matriz de SPNs para várias instâncias de serviço que serão executadas no mesmo host. Cada SPN especifica o nome do host e um número de porta para uma instância de serviço.

A matriz de nomes retornada por [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve ser liberada chamando a função [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .

Lembre-se de que as funções [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) não verificam se os SPNs são exclusivos. Como a autenticação mútua falhará se um cliente apresentar um SPN que não é exclusivo, verifique a exclusividade antes de registrar um SPN. Para fazer isso, pesquise o catálogo global (GC) em busca de atributos de **servicePrincipalName** que correspondam ao seu SPN. Para obter mais informações sobre como pesquisar o GC, consulte [pesquisando o catálogo global](searching-global-catalog-contents.md).

 

 




