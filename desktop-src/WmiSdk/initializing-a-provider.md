---
description: Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que seu provedor deve executar que permite enviar e receber informações do WMI, controlar um objeto gerenciado e executar outras tarefas.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inicializando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e373cf72d4715919a9d7fc59064d156e80a1f2371c585d698a7c6edff4f22fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097276"
---
# <a name="initializing-a-provider"></a>Inicializando um provedor

Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que seu provedor deve executar que permite enviar e receber informações do WMI, controlar um objeto gerenciado e executar outras tarefas. Cada tipo de provedor tem um conjunto diferente de tarefas que ele deve executar e tem um conjunto de interfaces exclusivas.

No entanto, todos os provedores inicializam por meio da interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informam o WMI sobre seu status de inicialização por meio da interface [**IWbemProviderInitSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)

O procedimento a seguir descreve como inicializar um provedor.

**Para inicializar um provedor**

1.  Implemente [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) para seu provedor.

    Quando o WMI determina que um cliente requer os serviços de um provedor, o WMI carrega o provedor chamando o método [**IWbemProviderInit::Initialize.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)

2.  Implemente qualquer interface exclusiva para seu tipo de provedor.
3.  Informe ao WMI que seu provedor foi concluído com a inicialização chamando [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Todas as implementações de [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devem chamar [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para relatar o status de inicialização para o WMI. O **método SetStatus** permite que o WMI determine se um provedor está pronto para receber solicitações e o tipo de solicitações que o provedor está pronto para receber.

O procedimento a seguir descreve como relatar uma inicialização bem-sucedida.

**Para relatar uma inicialização bem-sucedida**

-   De definir *o parâmetro IStatus* [**de SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) como **WBEM \_ S \_ INITIALIZED.**

    Ao retornar **o WBEM \_ S \_ INITIALIZED,** um provedor indica uma preparação para lidar com solicitações de aplicativos, WMI e outros provedores. Depois de receber o WBEM S INITIALIZED, o WMI faz uma chamada para o método \_ \_ [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) no provedor. Essa consulta recupera um ponteiro para a interface primária do provedor.

O procedimento a seguir descreve como relatar um erro durante a inicialização.

**Para relatar um erro durante a inicialização**

-   De definir *o parâmetro IStatus* [**de SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) como **WBEM \_ E \_ FAILED.** Provedores de exibições WMI que **retornam WBEM \_ E \_ FAILED** como não funcionais.

    O WMI libera o ponteiro [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) depois que o WMI tiver obtido um ponteiro para a interface primária do provedor ou após a falha na inicialização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Definindo Descritores de Segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Proteger seu provedor](securing-your-provider.md)
</dt> </dl>

 

 



