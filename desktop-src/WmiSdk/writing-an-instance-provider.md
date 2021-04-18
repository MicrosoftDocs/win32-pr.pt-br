---
description: Um provedor de instância fornece instâncias de uma ou mais classes fornecidas.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Gravando um provedor de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764508"
---
# <a name="writing-an-instance-provider"></a>Gravando um provedor de instância

Um provedor de instância fornece instâncias de uma ou mais classes fornecidas. Por exemplo, um provedor de instância pode fornecer informações sobre uma CPU ou outro tipo de hardware. Como os objetos gerenciados por um provedor de instância tendem a ser alterados regularmente, todos os provedores de instância são considerados provedores de pull; ou seja, um provedor que recupera dinamicamente informações sobre um objeto gerenciado sempre que o WMI faz uma solicitação para as informações. O nome vem da ideia de que o WMI "recebe" as informações do provedor em nome de uma solicitação do cliente. Usando a tecnologia pull, um provedor de instância pode dar suporte a recuperação, enumeração, modificação, exclusão e processamento de consulta de uma instância específica.

Provedores de alto desempenho podem aumentar a eficiência de um provedor de instância ou acessar programaticamente os dados que aparecem no monitor do sistema. Para obter mais informações, consulte [criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

O procedimento a seguir descreve como gravar um provedor de instância.

**Para gravar um provedor de instância**

1.  [Registre seu provedor com o WMI](registering-an-instance-provider.md).

    Os provedores de instância se registram com o WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

2.  [Inicialize seu provedor](initializing-a-provider.md).

    O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. Essa é uma tarefa comum a todos os provedores.

    > [!Note]  
    > Os provedores de instância são altamente incentivados a usar o modelo de vários threads "both".

     

3.  [Implemente a interface IWbemServices para seu provedor](implementing-the-primary-interface-for-an-instance-provider.md).

    A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de instância.

4.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI. Para obter mais informações, consulte [fazendo chamadas para o WMI](making-calls-to-wmi.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

5.  Se necessário, [implemente a interface de alto desempenho](improving-the-efficiency-of-an-instance-provider.md).

    A interface de alto desempenho aumenta a velocidade na qual o provedor pode reagir às solicitações do WMI.

6.  Se necessário, [implemente o suporte para atualizações de instância parcial](supporting-partial-instance-operations.md).

    Como o nome indica, uma atualização de instância parcial é uma técnica usada para atualizar apenas parte de uma instância. Para obter mais informações sobre como chamar uma instância parcial de um cliente, consulte [atualizando parte de uma instância](updating-part-of-an-instance.md) e [recuperando parte de uma instância do WMI](retrieving-part-of-an-instance.md).

7.  Substitua o provedor preexistente pelo seu novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar. Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).

 

 



