---
description: Um provedor de propriedades recupera e modifica valores de propriedade individuais para instâncias de uma determinada classe que é armazenada no repositório WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Gravando um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785272"
---
# <a name="writing-a-property-provider"></a>Gravando um provedor de propriedades

Um provedor de propriedades recupera e modifica valores de propriedade individuais para instâncias de uma determinada classe que é armazenada no repositório WMI.

O procedimento a seguir descreve como criar um provedor de propriedades.

**Para criar um provedor de propriedades**

1.  Projete e Registre seu provedor com o WMI.

    Os provedores de instância se registram com o WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) . Para obter mais informações, consulte [registrando um provedor de propriedades](registering-a-property-provider.md).

2.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. Essa é uma tarefa comum a todos os provedores. Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).

    > [!Note]  
    > Os provedores de propriedades são altamente incentivados a usar o modelo de vários threads "both".

     

3.  Implemente a interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) para seu provedor.

    A interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) é a interface primária para um provedor de propriedades. Os dois métodos principais são [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**putProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty). Para obter mais informações, consulte [implementando a interface primária para um provedor de propriedades](implementing-the-primary-interface-for-a-property-provider.md).

4.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI. Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

5.  Substitua o provedor preexistente pelo seu novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar. Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).

 

 



