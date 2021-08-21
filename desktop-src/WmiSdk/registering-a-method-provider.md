---
description: Para criar um provedor de método WMI, você deve registrar a instância Win32Provider que representa seu provedor usando uma instância \_ \_ \_ \_ de MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrando um provedor de método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a85fb93a30f6a996dd8e7255cc53f7a58a7fe37df35eb16bdca8de038e8704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992556"
---
# <a name="registering-a-method-provider"></a>Registrando um provedor de método

Para criar um provedor [*de*](gloss-m.md) método WMI, você deve registrar a instância [**\_ \_ win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Depois de criar uma instância [**\_ \_ do Win32Provider**](--win32provider.md), você deve registrar esse provedor com o WMI. Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressu que você já implementou o processo de registro, conforme descrito [em Registrando um provedor.](registering-a-provider.md)

O procedimento a seguir descreve como registrar um provedor de método.

**Para registrar um provedor de método**

1.  Crie uma instância da [**\_ \_ classe Win32Provider**](--win32provider.md) que descreve o provedor.

    A classe do sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration.**](--objectproviderregistration.md) No entanto, a única propriedade relevante para um provedor de método é o caminho do objeto para a instância [**\_ \_ Win32Provider.**](--win32provider.md)

2.  Crie uma instância da [**\_ \_ classe MethodProviderRegistration**](--methodproviderregistration.md) que descreve o conjunto de recursos do provedor.

    Certifique-se de marcar a classe com os qualificadores [**Dinâmico**](dynamic-qualifier.md) [**e**](/windows/desktop/api/Provider/nl-provider-provider) Provedor. O **qualificador** dinâmico sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe. O **qualificador** provedor especifica o nome do provedor que o WMI deve usar.

O exemplo de código a seguir descreve como registrar um provedor de método.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



