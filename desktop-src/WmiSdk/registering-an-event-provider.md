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
# <a name="registering-an-event-provider"></a><span data-ttu-id="9bb18-103">Registrando um provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="9bb18-103">Registering an Event Provider</span></span>

<span data-ttu-id="9bb18-104">Para criar um [*provedor de eventos*](gloss-e.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="9bb18-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="9bb18-105">Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI.</span><span class="sxs-lookup"><span data-stu-id="9bb18-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="9bb18-106">O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9bb18-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9bb18-107">O procedimento a seguir descreve como registrar um provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="9bb18-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="9bb18-108">**Para registrar um provedor de eventos**</span><span class="sxs-lookup"><span data-stu-id="9bb18-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="9bb18-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.</span><span class="sxs-lookup"><span data-stu-id="9bb18-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="9bb18-110">Crie uma instância da classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="9bb18-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="9bb18-111">A classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb18-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="9bb18-112">As propriedades local para a classe **\_ \_ EventProviderRegistration** são o caminho do objeto para o provedor e uma lista de consultas que descrevem os eventos aos quais o provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="9bb18-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="9bb18-113">Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9bb18-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="9bb18-114">Carregue a implementação das classes [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="9bb18-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="9bb18-115">O WMI usa sua definição de classe para registrar e acessar seu provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="9bb18-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="9bb18-116">Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9bb18-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9bb18-117">O exemplo de código a seguir descreve uma implementação de uma classe [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb18-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

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

<span data-ttu-id="9bb18-118">A primeira consulta indica que o provedor gera todas as notificações de evento para a classe de evento extrínsecos FaxEvent.</span><span class="sxs-lookup"><span data-stu-id="9bb18-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="9bb18-119">Como ele usa o operador ISA, a segunda consulta implica que o provedor gera notificações para todos os eventos de criação de instância para a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e todas as suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="9bb18-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="9bb18-120">Quando um provedor registra para fornecer um evento intrínseco, o evento deve ser aplicado a todas as instâncias de uma classe.</span><span class="sxs-lookup"><span data-stu-id="9bb18-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="9bb18-121">Em outras palavras, uma consulta não pode ser gravada para fornecer eventos de criação de instância para apenas algumas das unidades de disco que pertencem à classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="9bb18-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
