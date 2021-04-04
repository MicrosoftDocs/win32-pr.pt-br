---
description: Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que o seu provedor deve executar, permitindo que ele envie e receba informações do WMI, controle um objeto gerenciado e execute outras tarefas.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inicializando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837255"
---
# <a name="initializing-a-provider"></a>Inicializando um provedor

Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que o seu provedor deve executar, permitindo que ele envie e receba informações do WMI, controle um objeto gerenciado e execute outras tarefas. Cada tipo de provedor tem um conjunto diferente de tarefas que ele deve executar e tem um conjunto complementar de interfaces exclusivas.

No entanto, todos os provedores são inicializados por meio da interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informam o WMI sobre o status de inicialização por meio da interface [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .

O procedimento a seguir descreve como inicializar um provedor.

**Para inicializar um provedor**

1.  Implemente [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) para seu provedor.

    Quando o WMI determina que um cliente requer os serviços de um provedor, o WMI carrega o provedor chamando o método [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Implemente qualquer interface exclusiva para seu tipo de provedor.
3.  Informe ao WMI que seu provedor foi concluído com a inicialização chamando [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Todas as implementações de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devem chamar [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para relatar o status de inicialização para o WMI. O método **SetStatus** permite que o WMI determine se um provedor está pronto para receber solicitações e o tipo de solicitações que o provedor está pronto para receber.

O procedimento a seguir descreve como relatar uma inicialização bem-sucedida.

**Para relatar uma inicialização bem-sucedida**

-   Defina o parâmetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para **WBEM \_ S \_ INITIALIZED**.

    Ao retornar o **WBEM \_ S \_ inicializado**, um provedor indica uma prontidão para lidar com solicitações de aplicativos, WMI e outros provedores. Depois de receber \_ o WBEM S \_ inicializado, o WMI faz uma chamada para o método [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) no provedor. Essa consulta recupera um ponteiro para a interface primária do provedor.

O procedimento a seguir descreve como relatar um erro durante a inicialização.

**Para relatar um erro durante a inicialização**

-   Defina o parâmetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) como **WBEM \_ E \_ falhou**. Os provedores de exibições WMI que retornam **WBEM \_ E \_ falharam** como não funcionais.

    O WMI libera o ponteiro [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) após o WMI ter obtido um ponteiro para a interface primária do provedor ou após a inicialização falhar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> </dl>

 

 



