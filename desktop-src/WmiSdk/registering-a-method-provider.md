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
# <a name="registering-a-method-provider"></a><span data-ttu-id="9c44b-103">Registrando um provedor de métodos</span><span class="sxs-lookup"><span data-stu-id="9c44b-103">Registering a Method Provider</span></span>

<span data-ttu-id="9c44b-104">Para criar um [*provedor de métodos*](gloss-m.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="9c44b-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="9c44b-105">Depois de criar uma instância do [**\_ \_ Win32Provider**](--win32provider.md), você deve registrar esse provedor com o WMI.</span><span class="sxs-lookup"><span data-stu-id="9c44b-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="9c44b-106">Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI.</span><span class="sxs-lookup"><span data-stu-id="9c44b-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="9c44b-107">O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c44b-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="9c44b-108">O procedimento a seguir descreve como registrar um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="9c44b-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="9c44b-109">**Para registrar um provedor de métodos**</span><span class="sxs-lookup"><span data-stu-id="9c44b-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="9c44b-110">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.</span><span class="sxs-lookup"><span data-stu-id="9c44b-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="9c44b-111">A classe de sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , no entanto, a única propriedade relevante para um provedor de método é o caminho do objeto para a instância do [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="9c44b-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="9c44b-112">Crie uma instância da classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="9c44b-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="9c44b-113">Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="9c44b-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="9c44b-114">O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="9c44b-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="9c44b-115">O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.</span><span class="sxs-lookup"><span data-stu-id="9c44b-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="9c44b-116">O exemplo de código a seguir descreve como registrar um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="9c44b-116">The following code example describes how to register a method provider.</span></span>

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

 

 



