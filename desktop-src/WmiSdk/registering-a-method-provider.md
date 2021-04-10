---
description: Para criar um provedor de métodos WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrando um provedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170379"
---
# <a name="registering-a-method-provider"></a>Registrando um provedor de métodos

Para criar um [*provedor de métodos*](gloss-m.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Depois de criar uma instância do [**\_ \_ Win32Provider**](--win32provider.md), você deve registrar esse provedor com o WMI. Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de métodos.

**Para registrar um provedor de métodos**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.

    A classe de sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , no entanto, a única propriedade relevante para um provedor de método é o caminho do objeto para a instância do [**\_ \_ Win32Provider**](--win32provider.md) .

2.  Crie uma instância da classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) que descreve o conjunto de recursos do provedor.

    Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe. O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.

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

 

 



