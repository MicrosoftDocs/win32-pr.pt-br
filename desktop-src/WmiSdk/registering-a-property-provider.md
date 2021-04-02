---
description: Para criar um provedor de propriedades WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrando um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165218"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="d8ae9-103">Registrando um provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="d8ae9-103">Registering a Property Provider</span></span>

<span data-ttu-id="d8ae9-104">Para criar um [*provedor de propriedades*](gloss-p.md) WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="d8ae9-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="d8ae9-105">Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="d8ae9-106">O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8ae9-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="d8ae9-107">O procedimento a seguir descreve como registrar um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="d8ae9-108">**Para registrar um provedor de propriedades**</span><span class="sxs-lookup"><span data-stu-id="d8ae9-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="d8ae9-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="d8ae9-110">A classe [**\_ \_ Win32Provider**](--win32provider.md) aceita os valores padrão para outras propriedades, como o valor **verdadeiro** para a propriedade **pura** .</span><span class="sxs-lookup"><span data-stu-id="d8ae9-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="d8ae9-111">Para obter mais informações, consulte [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8ae9-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="d8ae9-112">Crie uma instância da classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="d8ae9-113">A classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) herda muitas propriedades da classe pai [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que fornece valores Boolianos que indicam suporte para recursos específicos e uma matriz de cadeias de caracteres para indicar suporte de consulta.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="d8ae9-114">Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="d8ae9-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="d8ae9-115">O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor dinâmico para recuperar as instâncias de classe que contêm as propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="d8ae9-116">O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="d8ae9-117">O WMI chama NewQuery em um provedor de eventos quando um consumidor cliente registra uma consulta de filtro de eventos que contém referências a eventos com suporte pelo provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="d8ae9-118">Portanto, o provedor de eventos responsável por eventos de modificação de instância para a classe EmailClass pode ser configurado para gerar notificações somente para o remetente.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="d8ae9-119">Quando o provedor recebe uma consulta solicitando a notificação de alterações para a propriedade Subject, o provedor pode começar a gerar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="d8ae9-120">Nesse cenário, o WMI não é necessário para descartar as notificações que relatam apenas as alterações de destinatário.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="d8ae9-121">O exemplo de código MOF a seguir descreve as instâncias que podem ser usadas para registrar um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8ae9-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="d8ae9-122">Somente os administradores podem registrar ou excluir um provedor de propriedades criando uma instância de [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="d8ae9-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



