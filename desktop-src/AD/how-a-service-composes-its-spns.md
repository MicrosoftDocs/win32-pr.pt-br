---
title: Como um serviço compõe seus SPNs
description: Um serviço pode usar duas funções para compor seus SPNs DsGetSpn é uma função de uso geral para compor SPNs e DsServerRegisterSpn é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome da entidade de serviço AD, como um serviço é composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb659eec3bb2d0f50fd109b39f356df1429535
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881393"
---
# <a name="how-a-service-composes-its-spns"></a>Como um serviço compõe seus SPNs

Um serviço pode usar duas funções para compor seus SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) é uma função de uso geral para compor SPNs e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.

Um instalador de serviço normalmente usa a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor SPNs, que ele registra na conta de logon do serviço usando a [**função DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) O **DsGetSpn** pode executar as seguintes funções.

-   Crie um SPN simples com o formato " <service class> / &lt; host " para um &gt; serviço baseado em host.
-   Crie um SPN complexo que inclua o componente " nome do serviço " usado por serviços relicáveis ou o componente " porta " que distingue várias instâncias de um serviço em um &lt; &gt; único &lt; &gt; host.
-   Crie um único SPN com o componente " host " definido como o nome de um host especificado ou o nome do &lt; &gt; computador local por padrão.
-   Crie uma matriz de SPNs para várias instâncias de serviço que serão executados em vários hosts em toda a floresta. Cada SPN especifica o nome do host para uma instância de serviço.
-   Crie uma matriz de SPNs para várias instâncias de serviço que serão executados no mesmo host. Cada SPN especifica o nome do host e um número da porta para uma instância de serviço.

A matriz de nomes [**retornados por DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve ser liberada chamando a [**função DsFreeSpnArray.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)

Esteja ciente de que as funções [**DsGetSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) não verificam se os SPNs são exclusivos. Como a autenticação mútua falhará se um cliente apresentar um SPN que não seja exclusivo, verifique a exclusividade antes de registrar um SPN. Para fazer isso, pesquise os atributos **servicePrincipalName** do catálogo global (GC) que corresponderem ao SPN. Para obter mais informações sobre como pesquisar o GC, consulte [Pesquisando o Catálogo Global.](searching-global-catalog-contents.md)

 

 




