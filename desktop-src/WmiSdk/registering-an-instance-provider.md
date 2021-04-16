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
# <a name="registering-an-instance-provider"></a><span data-ttu-id="2dc99-103">Registrando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="2dc99-103">Registering an Instance Provider</span></span>

<span data-ttu-id="2dc99-104">Para criar um [*provedor de instância*](gloss-i.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="2dc99-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="2dc99-105">Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc99-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="2dc99-106">O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2dc99-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="2dc99-107">O procedimento a seguir descreve como registrar um provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="2dc99-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="2dc99-108">**Para registrar um provedor de instância**</span><span class="sxs-lookup"><span data-stu-id="2dc99-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="2dc99-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.</span><span class="sxs-lookup"><span data-stu-id="2dc99-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="2dc99-110">Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="2dc99-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="2dc99-111">A classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que fornece valores Boolianos que indicam suporte para recursos específicos e uma matriz de cadeias de caracteres para indicar suporte de consulta.</span><span class="sxs-lookup"><span data-stu-id="2dc99-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="2dc99-112">Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](standard-wmi-qualifiers.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="2dc99-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="2dc99-113">O qualificador sinaliza que o WMI deve usar um provedor **dinâmico** para recuperar as instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="2dc99-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="2dc99-114">O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.</span><span class="sxs-lookup"><span data-stu-id="2dc99-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="2dc99-115">O exemplo de código a seguir descreve como registrar uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="2dc99-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

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

 

 



