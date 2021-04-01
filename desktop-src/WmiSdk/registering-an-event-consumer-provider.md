---
description: Para criar um provedor de consumidor de eventos WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrando um provedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661768"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="94397-103">Registrando um provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="94397-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="94397-104">Para criar um [*provedor de consumidor de eventos*](gloss-e.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="94397-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="94397-105">Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI.</span><span class="sxs-lookup"><span data-stu-id="94397-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="94397-106">O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="94397-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="94397-107">O procedimento a seguir descreve como registrar um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="94397-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="94397-108">**Para registrar um provedor de consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="94397-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="94397-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.</span><span class="sxs-lookup"><span data-stu-id="94397-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="94397-110">Crie uma instância da classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="94397-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="94397-111">As propriedades definidas por [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluem o caminho do objeto para o provedor e os nomes das classes de consumidor lógicas que o provedor de consumidor de eventos suporta.</span><span class="sxs-lookup"><span data-stu-id="94397-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="94397-112">Certifique-se de marcar a classe com os qualificadores **dinâmicos** e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="94397-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="94397-113">O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="94397-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="94397-114">O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.</span><span class="sxs-lookup"><span data-stu-id="94397-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="94397-115">O exemplo de código a seguir mostra como registrar um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="94397-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



