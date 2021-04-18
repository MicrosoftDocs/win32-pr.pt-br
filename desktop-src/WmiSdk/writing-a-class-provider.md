---
description: Um provedor de classe gerencia uma classe ou uma série de classes para o WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Escrevendo um provedor de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815535"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="8ceca-103">Escrevendo um provedor de classe</span><span class="sxs-lookup"><span data-stu-id="8ceca-103">Writing a Class Provider</span></span>

<span data-ttu-id="8ceca-104">Um provedor de classe gerencia uma classe ou uma série de classes para o WMI.</span><span class="sxs-lookup"><span data-stu-id="8ceca-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="8ceca-105">Um provedor de classe pode ser Push ou pull; ou seja, ele pode armazenar seus próprios dados ou permitir que o WMI armazene dados para ele no serviço de gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ceca-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="8ceca-106">Embora um provedor de classes seja instalado em um computador específico, ele pode alterar as definições de classe em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="8ceca-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="8ceca-107">Portanto, a maioria dos desenvolvedores geralmente não cria provedores de classe.</span><span class="sxs-lookup"><span data-stu-id="8ceca-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="8ceca-108">Antes de construir um provedor de classe, verifique se as classes com suporte realmente devem ser geradas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8ceca-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="8ceca-109">Na maioria dos casos, a lista de classes é uma alteração lenta e finita.</span><span class="sxs-lookup"><span data-stu-id="8ceca-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="8ceca-110">Se esse for o caso, você não precisará criar um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="8ceca-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="8ceca-111">Em vez disso, você pode posicionar as definições de classe no repositório WMI usando a API WMI ou um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="8ceca-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="8ceca-112">O procedimento a seguir descreve como implementar um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="8ceca-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="8ceca-113">**Para implementar um provedor de classe**</span><span class="sxs-lookup"><span data-stu-id="8ceca-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="8ceca-114">Determine se seu provedor é um provedor de Push ou pull.</span><span class="sxs-lookup"><span data-stu-id="8ceca-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="8ceca-115">Um provedor de pull fornece dados dinamicamente em resposta a uma solicitação de aplicativo, enquanto os provedores de push armazenam seus dados uma vez no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="8ceca-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="8ceca-116">Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="8ceca-117">Projete e Registre seu provedor de classes com o WMI.</span><span class="sxs-lookup"><span data-stu-id="8ceca-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="8ceca-118">Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma instância de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="8ceca-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="8ceca-119">Para obter mais informações, consulte [registrando um provedor de classe](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="8ceca-120">Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="8ceca-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="8ceca-121">O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="8ceca-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="8ceca-122">Se você estiver criando um provedor de push, **IWbemProviderInit** será a única interface que você implementará.</span><span class="sxs-lookup"><span data-stu-id="8ceca-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="8ceca-123">Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="8ceca-124">Os provedores de classe são altamente incentivados a usar o modelo de vários threads "both".</span><span class="sxs-lookup"><span data-stu-id="8ceca-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="8ceca-125">Adicione qualquer código adicional necessário para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="8ceca-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="8ceca-126">Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="8ceca-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="8ceca-127">Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="8ceca-128">Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="8ceca-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="8ceca-129">Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="8ceca-130">Implemente a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="8ceca-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="8ceca-131">A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de classe pull.</span><span class="sxs-lookup"><span data-stu-id="8ceca-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="8ceca-132">Para obter mais informações, consulte [implementando a interface primária para um provedor de classe](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="8ceca-133">Substitua o provedor preexistente pelo seu novo código.</span><span class="sxs-lookup"><span data-stu-id="8ceca-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="8ceca-134">Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar.</span><span class="sxs-lookup"><span data-stu-id="8ceca-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="8ceca-135">Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8ceca-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



