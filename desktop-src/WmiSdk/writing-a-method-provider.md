---
description: Um provedor de método permite que o WMI acesse os métodos de uma classe. Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escrevendo um provedor de método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea5121d4a9438744ad62b666e62d4ffa90c39428020d3e39c80a6de26e295959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311925"
---
# <a name="writing-a-method-provider"></a>Escrevendo um provedor de método

Um provedor de método permite que o WMI acesse os métodos de uma classe. Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.

Alterar a ordem dos parâmetros de entrada e saída do método ao atualizar um provedor de método existente pode causar falha para aplicativos que chamam o método . A ordem dos parâmetros de entrada ou saída é estabelecida pelo valor do qualificador [**de ID**](standard-wmi-qualifiers.md) em cada parâmetro. O primeiro parâmetro tem um **valor de ID** de zero. Adicione novos parâmetros de entrada ao final dos parâmetros existentes em vez de inseri-los na sequência já estabelecida.

O procedimento a seguir descreve como implementar um provedor de método.

**Para implementar um provedor de método**

1.  Projete e registre seu provedor de classe com o WMI.

    Os provedores de classe se registram no WMI criando uma [**\_ \_ instância win32Provider**](--win32provider.md) e uma [**\_ \_ classe MethodProviderRegistration.**](--methodproviderregistration.md) Para obter mais informações, consulte [Registrando um provedor de método](registering-a-method-provider.md).

2.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    > [!Note]  
    > Os provedores de método são fortemente incentivados a usar o modelo multithreading "Both".

     

3.  Implemente [**o método IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para seu provedor.

    A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface primária para um provedor de método. Para obter mais informações, [consulte Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).

4.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar interfaces WMI. Para obter mais informações, consulte [Chamando um método e](calling-a-method.md) mantendo níveis de segurança em um [provedor](impersonating-a-client.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança desse cliente. Para obter mais informações, consulte [Representando um cliente](impersonating-a-client.md).

5.  Substitua o provedor preexistência pelo novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistência para copiar. Para obter mais informações, consulte [Atualizando um provedor](updating-a-provider.md).

 

 



