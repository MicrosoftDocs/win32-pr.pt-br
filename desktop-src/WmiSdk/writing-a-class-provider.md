---
description: Um provedor de classe gerencia uma classe ou uma série de classes para o WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Escrevendo um provedor de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45815c795b6f43f3e7ec99b9ce9535c4d14b2bc8426ea5ca6b44f736415bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311935"
---
# <a name="writing-a-class-provider"></a>Escrevendo um provedor de classe

Um provedor de classe gerencia uma classe ou uma série de classes para o WMI. Um provedor de classe pode ser Push ou pull; ou seja, ele pode armazenar seus próprios dados ou permitir que o WMI armazene dados para ele no serviço de gerenciamento de Windows. Embora um provedor de classes seja instalado em um computador específico, ele pode alterar as definições de classe em toda a empresa. Portanto, a maioria dos desenvolvedores geralmente não cria provedores de classe.

Antes de construir um provedor de classe, verifique se as classes com suporte realmente devem ser geradas dinamicamente. Na maioria dos casos, a lista de classes é uma alteração lenta e finita. Se esse for o caso, você não precisará criar um provedor de classe. Em vez disso, você pode posicionar as definições de classe no repositório WMI usando a API WMI ou um arquivo MOF.

O procedimento a seguir descreve como implementar um provedor de classe.

**Para implementar um provedor de classe**

1.  Determine se seu provedor é um provedor de Push ou pull.

    Um provedor de pull fornece dados dinamicamente em resposta a uma solicitação de aplicativo, enquanto os provedores de push armazenam seus dados uma vez no repositório do WMI. Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).

2.  Projete e Registre seu provedor de classes com o WMI.

    Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma instância de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) . Para obter mais informações, consulte [registrando um provedor de classe](registering-a-class-provider.md).

3.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. Se você estiver criando um provedor de push, **IWbemProviderInit** será a única interface que você implementará. Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).

    > [!Note]  
    > Os provedores de classe são altamente incentivados a usar o modelo de vários threads "both".

     

4.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI. Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

5.  Implemente a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para seu provedor.

    A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de classe pull. Para obter mais informações, consulte [implementando a interface primária para um provedor de classe](implementing-the-primary-interface-for-a-class-provider.md).

6.  Substitua o provedor preexistente pelo seu novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar. Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).

 

 



