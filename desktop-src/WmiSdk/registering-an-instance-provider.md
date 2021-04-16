---
description: Para criar um provedor de instância WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrando um provedor de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505677"
---
# <a name="registering-an-instance-provider"></a>Registrando um provedor de instância

Para criar um [*provedor de instância*](gloss-i.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de instância.

**Para registrar um provedor de instância**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.
2.  Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que descreve o conjunto de recursos do provedor.

    A classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que fornece valores Boolianos que indicam suporte para recursos específicos e uma matriz de cadeias de caracteres para indicar suporte de consulta.

    Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](standard-wmi-qualifiers.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador sinaliza que o WMI deve usar um provedor **dinâmico** para recuperar as instâncias de classe. O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.

O exemplo de código a seguir descreve como registrar uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



