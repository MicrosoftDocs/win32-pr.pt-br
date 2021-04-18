---
description: O provedor de registro do sistema é registrado como parte do processo de instalação do WMI no Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registrando o provedor de registro do sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810854"
---
# <a name="registering-the-system-registry-provider"></a>Registrando o provedor de registro do sistema

O provedor de registro do sistema é registrado como parte do processo de instalação do WMI no Windows. Se você estiver usando outra plataforma e quiser usar o provedor de registro do sistema, primeiro deverá registrar o provedor seguindo as etapas descritas abaixo.

O procedimento a seguir descreve como registrar o provedor de registro do sistema.

**Para registrar o provedor de registro do sistema**

1.  Registre o provedor como um servidor COM.

    Se necessário, talvez seja necessário criar entradas do registro. Esse processo se aplica a todos os servidores COM e não está relacionado ao WMI. Para obter mais informações, consulte a documentação [com](https://msdn.microsoft.com/library/aa139695.aspx) no SDK (Software Development Kit) do Microsoft Windows.

2.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) para descrever a implementação do provedor de registro do sistema.

    A instância do [**\_ \_ Win32Provider**](--win32provider.md) descreve o nome do provedor e seu identificador de classe (**CLSID**).

    O exemplo a seguir descreve como registrar o [**\_ \_ Win32Provider**](--win32provider.md) como um provedor de método, evento ou propriedade de instância.

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  Crie uma ou mais instâncias de classes derivadas da classe [**\_ \_ ProviderRegistration**](--providerregistration.md) para descrever a implementação lógica do provedor de registro do sistema.

    Dependendo da finalidade para a qual você está registrando o provedor de registro do sistema, você pode criar uma ou mais das classes a seguir.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    O exemplo de código MOF a seguir descreve como você pode registrar o provedor de registro do sistema como uma instância, propriedade, evento ou provedor de método.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  Compile o arquivo MOF usando o compilador MOF ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

O arquivo RegEvent. mof fornecido na seção WMI do SDK do Windows contém as instâncias [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necessárias para registrar o provedor de registro do sistema como um provedor de eventos. Para obter mais informações sobre como registrar um provedor, consulte [registrando um provedor](registering-a-provider.md) e [recebendo um evento WMI](receiving-a-wmi-event.md).

 

 



