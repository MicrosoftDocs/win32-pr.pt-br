---
description: Um provedor de método permite o acesso de WMI aos métodos de uma classe. Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escrevendo um provedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761693"
---
# <a name="writing-a-method-provider"></a>Escrevendo um provedor de métodos

Um provedor de método permite o acesso de WMI aos métodos de uma classe. Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.

Alterar a ordem dos parâmetros de entrada e saída do método ao atualizar um provedor de métodos existente pode causar falha em aplicativos que chamam o método. A ordem dos parâmetros de entrada ou saída é estabelecida pelo valor do qualificador de [**ID**](standard-wmi-qualifiers.md) em cada parâmetro. O primeiro parâmetro tem um valor de **ID** igual a zero. Adicione novos parâmetros de entrada ao final dos parâmetros existentes em vez de inseri-los na sequência já estabelecida.

O procedimento a seguir descreve como implementar um provedor de método.

**Para implementar um provedor de métodos**

1.  Projete e Registre seu provedor de classes com o WMI.

    Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) . Para obter mais informações, consulte [registrando um provedor de método](registering-a-method-provider.md).

2.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    > [!Note]  
    > Os provedores de método são altamente incentivados a usar o modelo de vários threads "both".

     

3.  Implemente o método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para seu provedor.

    A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de métodos. Para obter mais informações, consulte [implementando a interface primária para um provedor de métodos](implementing-the-primary-interface-for-a-method-provider.md).

4.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI. Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

5.  Substitua o provedor preexistente pelo seu novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar. Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).

 

 



