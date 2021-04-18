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
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="57728-103">Registrando o provedor de registro do sistema</span><span class="sxs-lookup"><span data-stu-id="57728-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="57728-104">O provedor de registro do sistema é registrado como parte do processo de instalação do WMI no Windows.</span><span class="sxs-lookup"><span data-stu-id="57728-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="57728-105">Se você estiver usando outra plataforma e quiser usar o provedor de registro do sistema, primeiro deverá registrar o provedor seguindo as etapas descritas abaixo.</span><span class="sxs-lookup"><span data-stu-id="57728-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="57728-106">O procedimento a seguir descreve como registrar o provedor de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="57728-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="57728-107">**Para registrar o provedor de registro do sistema**</span><span class="sxs-lookup"><span data-stu-id="57728-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="57728-108">Registre o provedor como um servidor COM.</span><span class="sxs-lookup"><span data-stu-id="57728-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="57728-109">Se necessário, talvez seja necessário criar entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="57728-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="57728-110">Esse processo se aplica a todos os servidores COM e não está relacionado ao WMI.</span><span class="sxs-lookup"><span data-stu-id="57728-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="57728-111">Para obter mais informações, consulte a documentação [com](https://msdn.microsoft.com/library/aa139695.aspx) no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="57728-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="57728-112">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) para descrever a implementação do provedor de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="57728-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="57728-113">A instância do [**\_ \_ Win32Provider**](--win32provider.md) descreve o nome do provedor e seu identificador de classe (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="57728-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="57728-114">O exemplo a seguir descreve como registrar o [**\_ \_ Win32Provider**](--win32provider.md) como um provedor de método, evento ou propriedade de instância.</span><span class="sxs-lookup"><span data-stu-id="57728-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

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

3.  <span data-ttu-id="57728-115">Crie uma ou mais instâncias de classes derivadas da classe [**\_ \_ ProviderRegistration**](--providerregistration.md) para descrever a implementação lógica do provedor de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="57728-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="57728-116">Dependendo da finalidade para a qual você está registrando o provedor de registro do sistema, você pode criar uma ou mais das classes a seguir.</span><span class="sxs-lookup"><span data-stu-id="57728-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="57728-117">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="57728-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="57728-118">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="57728-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="57728-119">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="57728-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="57728-120">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="57728-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="57728-121">O exemplo de código MOF a seguir descreve como você pode registrar o provedor de registro do sistema como uma instância, propriedade, evento ou provedor de método.</span><span class="sxs-lookup"><span data-stu-id="57728-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

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

4.  <span data-ttu-id="57728-122">Compile o arquivo MOF usando o compilador MOF ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="57728-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="57728-123">O arquivo RegEvent. mof fornecido na seção WMI do SDK do Windows contém as instâncias [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necessárias para registrar o provedor de registro do sistema como um provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="57728-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="57728-124">Para obter mais informações sobre como registrar um provedor, consulte [registrando um provedor](registering-a-provider.md) e [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="57728-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



