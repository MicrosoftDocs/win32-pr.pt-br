---
description: Um provedor de propriedades recupera e modifica valores de propriedade individuais para instâncias de uma determinada classe que é armazenada no repositório WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Gravando um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785272"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="e31c2-103">Gravando um provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="e31c2-103">Writing a Property Provider</span></span>

<span data-ttu-id="e31c2-104">Um provedor de propriedades recupera e modifica valores de propriedade individuais para instâncias de uma determinada classe que é armazenada no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="e31c2-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="e31c2-105">O procedimento a seguir descreve como criar um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e31c2-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="e31c2-106">**Para criar um provedor de propriedades**</span><span class="sxs-lookup"><span data-stu-id="e31c2-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="e31c2-107">Projete e Registre seu provedor com o WMI.</span><span class="sxs-lookup"><span data-stu-id="e31c2-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="e31c2-108">Os provedores de instância se registram com o WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="e31c2-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="e31c2-109">Para obter mais informações, consulte [registrando um provedor de propriedades](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="e31c2-110">Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="e31c2-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="e31c2-111">O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="e31c2-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="e31c2-112">Essa é uma tarefa comum a todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="e31c2-112">This is a task common to all providers.</span></span> <span data-ttu-id="e31c2-113">Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="e31c2-114">Os provedores de propriedades são altamente incentivados a usar o modelo de vários threads "both".</span><span class="sxs-lookup"><span data-stu-id="e31c2-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="e31c2-115">Implemente a interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="e31c2-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="e31c2-116">A interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) é a interface primária para um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e31c2-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="e31c2-117">Os dois métodos principais são [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**putProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span><span class="sxs-lookup"><span data-stu-id="e31c2-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="e31c2-118">Para obter mais informações, consulte [implementando a interface primária para um provedor de propriedades](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="e31c2-119">Adicione qualquer código adicional necessário para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="e31c2-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="e31c2-120">Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="e31c2-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="e31c2-121">Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="e31c2-122">Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="e31c2-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="e31c2-123">Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="e31c2-124">Substitua o provedor preexistente pelo seu novo código.</span><span class="sxs-lookup"><span data-stu-id="e31c2-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="e31c2-125">Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar.</span><span class="sxs-lookup"><span data-stu-id="e31c2-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="e31c2-126">Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e31c2-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



