---
description: Um provedor de método permite o acesso de WMI aos métodos de uma classe. Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escrevendo um provedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761693"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="58c48-104">Escrevendo um provedor de métodos</span><span class="sxs-lookup"><span data-stu-id="58c48-104">Writing a Method Provider</span></span>

<span data-ttu-id="58c48-105">Um provedor de método permite o acesso de WMI aos métodos de uma classe.</span><span class="sxs-lookup"><span data-stu-id="58c48-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="58c48-106">Por exemplo, uma classe que representa um aplicativo pode ter um método que encerra o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58c48-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="58c48-107">Alterar a ordem dos parâmetros de entrada e saída do método ao atualizar um provedor de métodos existente pode causar falha em aplicativos que chamam o método.</span><span class="sxs-lookup"><span data-stu-id="58c48-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="58c48-108">A ordem dos parâmetros de entrada ou saída é estabelecida pelo valor do qualificador de [**ID**](standard-wmi-qualifiers.md) em cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="58c48-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="58c48-109">O primeiro parâmetro tem um valor de **ID** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="58c48-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="58c48-110">Adicione novos parâmetros de entrada ao final dos parâmetros existentes em vez de inseri-los na sequência já estabelecida.</span><span class="sxs-lookup"><span data-stu-id="58c48-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="58c48-111">O procedimento a seguir descreve como implementar um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="58c48-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="58c48-112">**Para implementar um provedor de métodos**</span><span class="sxs-lookup"><span data-stu-id="58c48-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="58c48-113">Projete e Registre seu provedor de classes com o WMI.</span><span class="sxs-lookup"><span data-stu-id="58c48-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="58c48-114">Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="58c48-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="58c48-115">Para obter mais informações, consulte [registrando um provedor de método](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58c48-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="58c48-116">Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="58c48-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="58c48-117">Os provedores de método são altamente incentivados a usar o modelo de vários threads "both".</span><span class="sxs-lookup"><span data-stu-id="58c48-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="58c48-118">Implemente o método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="58c48-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="58c48-119">A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="58c48-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="58c48-120">Para obter mais informações, consulte [implementando a interface primária para um provedor de métodos](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58c48-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="58c48-121">Adicione qualquer código adicional necessário para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="58c48-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="58c48-122">Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="58c48-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="58c48-123">Para obter mais informações, consulte [chamar um método](calling-a-method.md) e [manter níveis de segurança em um provedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="58c48-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="58c48-124">Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="58c48-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="58c48-125">Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="58c48-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="58c48-126">Substitua o provedor preexistente pelo seu novo código.</span><span class="sxs-lookup"><span data-stu-id="58c48-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="58c48-127">Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar.</span><span class="sxs-lookup"><span data-stu-id="58c48-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="58c48-128">Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58c48-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



