---
description: Para criar um provedor de eventos WMI, você deve registrar a instância win32Provider que representa seu provedor usando uma instância \_ \_ \_ \_ de EventProviderRegistration.
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
ms.openlocfilehash: 44c6521e56441c929ef108ce4c4b624c11b06ca26dc508c8f2f924e2f87babba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992506"
---
# <a name="registering-an-event-provider"></a>Registrando um provedor de eventos

Para criar um provedor [*de*](gloss-e.md) eventos WMI, você deve registrar a instância [**\_ \_ win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressu que você já implementou o processo de registro, conforme descrito [em Registrando um provedor.](registering-a-provider.md)

O procedimento a seguir descreve como registrar um provedor de eventos.

**Para registrar um provedor de eventos**

1.  Crie uma instância da [**\_ \_ classe Win32Provider**](--win32provider.md) que descreve o provedor.
2.  Crie uma instância da [**\_ \_ classe EventProviderRegistration**](--eventproviderregistration.md) que descreve o conjunto de recursos do provedor.

    A [**\_ \_ classe EventProviderRegistration**](--eventproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration.**](--objectproviderregistration.md) As propriedades locais para a **\_ \_ classe EventProviderRegistration** são o caminho do objeto para o provedor e uma lista de consultas que descrevem os eventos que o provedor dá suporte. Para obter mais informações, [consulte Consultando WMI](querying-wmi.md).

3.  Carregue sua implementação das [**\_ \_ classes Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) no repositório WMI.

    O WMI usa sua definição de classe para registrar e acessar seu provedor de eventos. Para obter mais informações, [consulte Registrando um provedor](registering-a-provider.md).

O exemplo de código a seguir descreve uma implementação de [**\_ \_ uma classe Win32Provider**](--win32provider.md) e uma [**\_ \_ classe EventProviderRegistration.**](--eventproviderregistration.md)

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

A primeira consulta indica que o provedor gera todas as notificações de evento para a classe de evento extrinsic FaxEvent. Como ele usa o operador ISA, a segunda consulta implica que o provedor gera notificações para todos os eventos de criação de instância para a classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e todas as suas subclasses.

Quando um provedor se registra para fornecer um evento intrínseco, o evento deve ser aplicado a todas as instâncias de uma classe. Em outras palavras, uma consulta não pode ser escrita para fornecer eventos de criação de instância para apenas algumas das unidades de disco que pertencem à [**classe \_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

 

 
