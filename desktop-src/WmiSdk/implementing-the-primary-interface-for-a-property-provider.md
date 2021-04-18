---
description: Um provedor de propriedades usa os métodos IWbemPropertyProvider como a interface primária para o WMI. Com o IWbemPropertyProvider, você pode implementar o código para recuperar e modificar as propriedades de classe e instância.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815568"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="b87c5-104">Implementando a interface primária para um provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="b87c5-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="b87c5-105">Um provedor de propriedades usa os métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) como a interface primária para o WMI.</span><span class="sxs-lookup"><span data-stu-id="b87c5-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="b87c5-106">Com o **IWbemPropertyProvider**, você pode implementar o código para recuperar e modificar as propriedades de classe e instância.</span><span class="sxs-lookup"><span data-stu-id="b87c5-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="b87c5-107">A tabela a seguir lista os métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que você pode implementar para um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b87c5-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="b87c5-108">Método</span><span class="sxs-lookup"><span data-stu-id="b87c5-108">Method</span></span>                                                   | <span data-ttu-id="b87c5-109">Recurso</span><span class="sxs-lookup"><span data-stu-id="b87c5-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="b87c5-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="b87c5-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="b87c5-111">Recuperação</span><span class="sxs-lookup"><span data-stu-id="b87c5-111">Retrieval</span></span>    |
| [<span data-ttu-id="b87c5-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="b87c5-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="b87c5-113">Modification</span><span class="sxs-lookup"><span data-stu-id="b87c5-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="b87c5-114">Você deve implementar um provedor de propriedades como um provedor em processo.</span><span class="sxs-lookup"><span data-stu-id="b87c5-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="b87c5-115">O WMI inicializará os provedores de propriedades gravados como serviços ou arquivos executáveis, mas nunca chamará seus métodos [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**putProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .</span><span class="sxs-lookup"><span data-stu-id="b87c5-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="b87c5-116">Se você optar por não oferecer suporte a um desses métodos, seu provedor poderá fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível**.</span><span class="sxs-lookup"><span data-stu-id="b87c5-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="b87c5-117">Um provedor de propriedades identifica uma classe ou instância gerenciada por um conjunto de três qualificadores: **PropertyContext**, **InstanceContext** e **ClassContext**.</span><span class="sxs-lookup"><span data-stu-id="b87c5-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="b87c5-118">O WMI passará constantes de cadeia de caracteres descrevendo esses três qualificadores para seu provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b87c5-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="b87c5-119">Seu provedor de propriedades deve estar preparado para lidar com os seguintes tipos de qualificadores de contexto:</span><span class="sxs-lookup"><span data-stu-id="b87c5-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="b87c5-120">O qualificador **InstanceContext** é anexado a uma instância e contém informações que se aplicam a todas as propriedades na instância.</span><span class="sxs-lookup"><span data-stu-id="b87c5-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="b87c5-121">O qualificador **ClassContext** é anexado a uma classe e contém informações que se aplicam a todas as instâncias na classe.</span><span class="sxs-lookup"><span data-stu-id="b87c5-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="b87c5-122">Por exemplo, em uma classe usada para armazenar dados fornecidos pelo provedor de registro, **ClassContext** pode ser o caminho para a chave do registro que contém as propriedades a serem relatadas.</span><span class="sxs-lookup"><span data-stu-id="b87c5-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="b87c5-123">O qualificador **PropertyContext** especifica informações específicas de contexto que pertencem à propriedade.</span><span class="sxs-lookup"><span data-stu-id="b87c5-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="b87c5-124">Por exemplo, em uma classe usada para armazenar dados fornecidos pelo provedor de registro, **PropertyContext** especifica o nome do valor do registro a ser armazenado pela propriedade.</span><span class="sxs-lookup"><span data-stu-id="b87c5-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="b87c5-125">Esses qualificadores podem trabalhar juntos.</span><span class="sxs-lookup"><span data-stu-id="b87c5-125">These qualifiers can work together.</span></span> <span data-ttu-id="b87c5-126">Você pode designar um valor de **InstanceContext** e **PropertyContext** para informar ao provedor como tratar tipos específicos de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b87c5-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="b87c5-127">Por exemplo, talvez você queira marcar instâncias que o provedor reconhecerá como legível, mas tendo apenas uma propriedade gravável.</span><span class="sxs-lookup"><span data-stu-id="b87c5-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="b87c5-128">O qualificador mais comum usado é **PropertyContext**.</span><span class="sxs-lookup"><span data-stu-id="b87c5-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="b87c5-129">Portanto, o WMI fornece o qualificador **DynProps** como um atalho.</span><span class="sxs-lookup"><span data-stu-id="b87c5-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="b87c5-130">O WMI considera que cada propriedade em uma instância marcada com **DynProps** também tem os qualificadores **dinâmico**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="b87c5-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



