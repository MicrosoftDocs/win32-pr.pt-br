---
description: Para criar um provedor de eventos WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrando um provedor de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091755"
---
# <a name="registering-an-event-provider"></a>Registrando um provedor de eventos

Para criar um [*provedor de eventos*](gloss-e.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de eventos.

**Para registrar um provedor de eventos**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.
2.  Crie uma instância da classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) que descreve o conjunto de recursos do provedor.

    A classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . As propriedades local para a classe **\_ \_ EventProviderRegistration** são o caminho do objeto para o provedor e uma lista de consultas que descrevem os eventos aos quais o provedor dá suporte. Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).

3.  Carregue a implementação das classes [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) no repositório do WMI.

    O WMI usa sua definição de classe para registrar e acessar seu provedor de eventos. Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).

O exemplo de código a seguir descreve uma implementação de uma classe [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

A primeira consulta indica que o provedor gera todas as notificações de evento para a classe de evento extrínsecos FaxEvent. Como ele usa o operador ISA, a segunda consulta implica que o provedor gera notificações para todos os eventos de criação de instância para a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e todas as suas subclasses.

Quando um provedor registra para fornecer um evento intrínseco, o evento deve ser aplicado a todas as instâncias de uma classe. Em outras palavras, uma consulta não pode ser gravada para fornecer eventos de criação de instância para apenas algumas das unidades de disco que pertencem à classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

 

 
