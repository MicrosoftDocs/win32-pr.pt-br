---
description: Quando um aplicativo de usuário solicita dados de objetos no sistema por meio de um provedor WMI, a representação significa que o provedor apresenta credenciais que representam o nível de segurança dos clientes em vez dos provedores.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Representando um cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829274"
---
# <a name="impersonating-a-client"></a><span data-ttu-id="114e6-103">Representando um cliente</span><span class="sxs-lookup"><span data-stu-id="114e6-103">Impersonating a Client</span></span>

<span data-ttu-id="114e6-104">Quando um aplicativo de usuário solicita dados de objetos no sistema por meio de um provedor WMI, a representação significa que o provedor apresenta as credenciais que representam o nível de segurança do cliente, em vez do provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-104">When a user application requests data from objects on the system through a WMI provider, impersonation means the provider presents credentials that represent the client's security level rather than the provider's.</span></span> <span data-ttu-id="114e6-105">A representação impede que um cliente obtenha acesso não autorizado às informações no sistema.</span><span class="sxs-lookup"><span data-stu-id="114e6-105">Impersonation prevents a client from obtaining unauthorized access to information on the system.</span></span>

<span data-ttu-id="114e6-106">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="114e6-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="114e6-107">Registrando um provedor para representação</span><span class="sxs-lookup"><span data-stu-id="114e6-107">Registering a Provider for Impersonation</span></span>](#registering-a-provider-for-impersonation)
-   [<span data-ttu-id="114e6-108">Definindo níveis de representação dentro de um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-108">Setting Impersonation Levels Within a Provider</span></span>](#setting-impersonation-levels-within-a-provider)
-   [<span data-ttu-id="114e6-109">Mantendo níveis de segurança em um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-109">Maintaining Security Levels in a Provider</span></span>](#maintaining-security-levels-in-a-provider)
-   [<span data-ttu-id="114e6-110">Manipulando mensagens de acesso negado em um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-110">Handling Access Denied Messages in a Provider</span></span>](#handling-access-denied-messages-in-a-provider)
-   [<span data-ttu-id="114e6-111">Relatórios de instâncias parciais</span><span class="sxs-lookup"><span data-stu-id="114e6-111">Reporting Partial Instances</span></span>](#reporting-partial-instances)
-   [<span data-ttu-id="114e6-112">Relatando enumerações parciais</span><span class="sxs-lookup"><span data-stu-id="114e6-112">Reporting Partial Enumerations</span></span>](#reporting-partial-enumerations)
-   [<span data-ttu-id="114e6-113">Depurando seu código de acesso negado</span><span class="sxs-lookup"><span data-stu-id="114e6-113">Debugging Your Access Denied Code</span></span>](#debugging-your-access-denied-code)
-   [<span data-ttu-id="114e6-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="114e6-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="114e6-115">Normalmente, o WMI é executado como um serviço administrativo em um nível de segurança alto, usando o contexto de segurança LocalServer.</span><span class="sxs-lookup"><span data-stu-id="114e6-115">WMI typically runs as an administrative service at a high security level, using the LocalServer security context.</span></span> <span data-ttu-id="114e6-116">O uso de um serviço administrativo fornece ao WMI o meio de acessar informações privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="114e6-116">Using an administrative service gives WMI the means to access privileged information.</span></span> <span data-ttu-id="114e6-117">Ao chamar um provedor para obter informações, o WMI passa seu SID (identificador de segurança) para o provedor, permitindo que o provedor acesse as informações no mesmo nível de segurança alto.</span><span class="sxs-lookup"><span data-stu-id="114e6-117">When calling a provider for information, WMI passes its security identifier (SID) to the provider, enabling the provider to access information at the same high security level.</span></span>

<span data-ttu-id="114e6-118">Durante o processo de inicialização do aplicativo WMI, o sistema operacional Windows fornece ao aplicativo WMI o contexto de segurança do usuário que iniciou o processo.</span><span class="sxs-lookup"><span data-stu-id="114e6-118">During the WMI application launch process, the Windows operating system gives the WMI application the security context of the user who began the process.</span></span> <span data-ttu-id="114e6-119">O contexto de segurança do usuário normalmente é um nível de segurança mais baixo do que LocalServer, portanto, o usuário pode não ter permissão para acessar todas as informações disponíveis para o WMI.</span><span class="sxs-lookup"><span data-stu-id="114e6-119">The security context of the user is typically a lower security level than LocalServer, so the user may not have permission to access all of the information available to WMI.</span></span> <span data-ttu-id="114e6-120">Quando o aplicativo do usuário solicita informações dinâmicas, o WMI passa o SID do usuário para o provedor correspondente.</span><span class="sxs-lookup"><span data-stu-id="114e6-120">When the user application asks for dynamic information, WMI passes the SID of the user to the corresponding provider.</span></span> <span data-ttu-id="114e6-121">Se for escrito adequadamente, o provedor tentará acessar informações com o SID do usuário, em vez do SID do provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-121">If written appropriately, the provider attempts to access information with the user SID, rather than the provider SID.</span></span>

<span data-ttu-id="114e6-122">Para que o provedor represente com êxito o aplicativo cliente, o aplicativo cliente e o provedor devem atender aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="114e6-122">For the provider to successfully impersonate the client application, the client application and provider must meet the following criteria:</span></span>

-   <span data-ttu-id="114e6-123">O aplicativo cliente deve chamar o WMI com um nível de segurança de conexão COM do destino de nível de **IMP do RPC \_ c \_ \_ \_** ou o delegado de nível de **IMP do RPC \_ c \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="114e6-123">The client application must call WMI with a COM connection security level of **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** or **RPC\_C\_IMP\_LEVEL\_DELEGATE**.</span></span> <span data-ttu-id="114e6-124">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="114e6-124">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>
-   <span data-ttu-id="114e6-125">O provedor deve se registrar no WMI como um provedor de representação.</span><span class="sxs-lookup"><span data-stu-id="114e6-125">The provider must register with WMI as an impersonation provider.</span></span> <span data-ttu-id="114e6-126">Para obter mais informações, consulte [registrando um provedor para representação](#registering-a-provider-for-impersonation).</span><span class="sxs-lookup"><span data-stu-id="114e6-126">For more information, see [Registering a Provider for Impersonation](#registering-a-provider-for-impersonation).</span></span>
-   <span data-ttu-id="114e6-127">O provedor deve alternar para o nível de segurança do aplicativo cliente antes de acessar informações privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="114e6-127">The provider must switch to the security level of the client application before accessing privileged information.</span></span> <span data-ttu-id="114e6-128">Para obter mais informações, consulte [definindo níveis de representação em um provedor](#setting-impersonation-levels-within-a-provider).</span><span class="sxs-lookup"><span data-stu-id="114e6-128">For more information, see [Setting Impersonation Levels Within a Provider](#setting-impersonation-levels-within-a-provider).</span></span>
-   <span data-ttu-id="114e6-129">O provedor deve lidar corretamente com condições de erro se o acesso a essas informações for negado.</span><span class="sxs-lookup"><span data-stu-id="114e6-129">The provider must correctly handle error conditions if access to this information is denied.</span></span> <span data-ttu-id="114e6-130">Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](#handling-access-denied-messages-in-a-provider).</span><span class="sxs-lookup"><span data-stu-id="114e6-130">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

## <a name="registering-a-provider-for-impersonation"></a><span data-ttu-id="114e6-131">Registrando um provedor para representação</span><span class="sxs-lookup"><span data-stu-id="114e6-131">Registering a Provider for Impersonation</span></span>

<span data-ttu-id="114e6-132">O WMI só passa o SID de um aplicativo cliente para provedores que se registraram como provedores de representação.</span><span class="sxs-lookup"><span data-stu-id="114e6-132">WMI only passes the SID of a client application to providers who have registered as impersonation providers.</span></span> <span data-ttu-id="114e6-133">A habilitação de um provedor para executar a representação requer que você modifique o processo de registro do provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-133">Enabling a provider to perform impersonation requires that you modify the provider registration process.</span></span>

<span data-ttu-id="114e6-134">O procedimento a seguir descreve como registrar um provedor para representação.</span><span class="sxs-lookup"><span data-stu-id="114e6-134">The following procedure describes how to register a provider for impersonation.</span></span> <span data-ttu-id="114e6-135">O procedimento pressupõe que você já entendeu o processo de registro.</span><span class="sxs-lookup"><span data-stu-id="114e6-135">The procedure assumes that you already understand the registration process.</span></span> <span data-ttu-id="114e6-136">Para obter mais informações sobre o processo de registro, consulte [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="114e6-136">For more information about the registration process, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="114e6-137">**Para registrar um provedor para representação**</span><span class="sxs-lookup"><span data-stu-id="114e6-137">**To register a provider for impersonation**</span></span>

1.  <span data-ttu-id="114e6-138">Defina a propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) da classe [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor como 1.</span><span class="sxs-lookup"><span data-stu-id="114e6-138">Set the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property of the [**\_\_Win32Provider**](--win32provider.md) class that represents your provider to 1.</span></span>

    <span data-ttu-id="114e6-139">A propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) documenta se o provedor oferece suporte à representação ou não.</span><span class="sxs-lookup"><span data-stu-id="114e6-139">The [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property documents whether the provider supports impersonation or not.</span></span> <span data-ttu-id="114e6-140">Definir **ImpersonationLevel** como 0 indica que o provedor não representa o cliente e executa todas as operações solicitadas no mesmo contexto de usuário que o WMI.</span><span class="sxs-lookup"><span data-stu-id="114e6-140">Setting **ImpersonationLevel** to 0 indicates that the provider does not impersonate the client and performs all requested operations in the same user context as WMI.</span></span> <span data-ttu-id="114e6-141">Definir **ImpersonationLevel** como 1 indica que o provedor usa chamadas de representação para verificar as operações executadas em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-141">Setting **ImpersonationLevel** to 1 indicates that the provider uses impersonation calls to check operations performed on behalf of the client.</span></span>

2.  <span data-ttu-id="114e6-142">Defina a propriedade **PerUserInitialization** da mesma classe [**\_ \_ Win32Provider**](--win32provider.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="114e6-142">Set the **PerUserInitialization** property of the same [**\_\_Win32Provider**](--win32provider.md) class to **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="114e6-143">Se você registrar um provedor com a propriedade [**\_ \_ Win32Provider**](--win32provider.md) **InitializeAsAdminFirst** definida como **true**, o provedor usará o token de segurança de thread de nível de administração somente durante a fase de inicialização.</span><span class="sxs-lookup"><span data-stu-id="114e6-143">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) property **InitializeAsAdminFirst** set to **TRUE**, then the provider uses the administration-level thread security token only during the initialization phase.</span></span> <span data-ttu-id="114e6-144">Embora uma chamada para [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) não falhe, o provedor usa o contexto de segurança do WMI e não do cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-144">While a call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not fail, the provider uses the security context of WMI and not of the client.</span></span>

 

<span data-ttu-id="114e6-145">O exemplo de código a seguir mostra como registrar um provedor para representação.</span><span class="sxs-lookup"><span data-stu-id="114e6-145">The following code example shows how to register a provider for impersonation.</span></span>

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a><span data-ttu-id="114e6-146">Definindo níveis de representação dentro de um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-146">Setting Impersonation Levels Within a Provider</span></span>

<span data-ttu-id="114e6-147">Se você registrar um provedor com a propriedade de classe [**\_ \_ Win32Provider**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) definida como 1, o WMI chamará seu provedor para representar vários clientes.</span><span class="sxs-lookup"><span data-stu-id="114e6-147">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) class property [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) set to 1, then WMI calls your provider to impersonate various clients.</span></span> <span data-ttu-id="114e6-148">Para lidar com essas chamadas, use as funções com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) em sua implementação da interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="114e6-148">To handle these calls, use the [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) COM functions in your implementation of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="114e6-149">A função [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) permite que um servidor represente o cliente que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="114e6-149">The [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) function allows a server to impersonate the client that made the call.</span></span> <span data-ttu-id="114e6-150">Ao fazer uma chamada para **CoImpersonateClient** em sua implementação de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), você permite que seu provedor defina o token de thread do provedor para corresponder ao token de thread do cliente e, portanto, representa o cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-150">By placing a call to **CoImpersonateClient** into your implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), you allow your provider to set the thread token of the provider to match the thread token of the client, and thus impersonate the client.</span></span> <span data-ttu-id="114e6-151">Se você não chamar **CoImpersonateClient**, seu provedor executará o código em um nível de segurança de administrador, criando assim uma vulnerabilidade de segurança em potencial.</span><span class="sxs-lookup"><span data-stu-id="114e6-151">If you do not call **CoImpersonateClient**, your provider executes code at an administrator level of security, thereby creating a potential security vulnerability.</span></span> <span data-ttu-id="114e6-152">Se o seu provedor precisar agir temporariamente como administrador ou executar a verificação de acesso manualmente, chame o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="114e6-152">If your provider temporarily needs to act as an administrator or perform the access check manually, then call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="114e6-153">Em contraste com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) é uma função com que lida com os níveis de representação do thread.</span><span class="sxs-lookup"><span data-stu-id="114e6-153">In contrast to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is a COM function that handles thread impersonation levels.</span></span> <span data-ttu-id="114e6-154">Nesse caso, o **CoRevertToSelf** altera o nível de representação de volta para a configuração de representação original.</span><span class="sxs-lookup"><span data-stu-id="114e6-154">In this case, **CoRevertToSelf** changes the impersonation level back to the original impersonation setting.</span></span> <span data-ttu-id="114e6-155">Em geral, o provedor é inicialmente um administrador e alterna entre **CoImpersonateClient** e **CoRevertToSelf** dependendo se ele está fazendo uma chamada que representa o chamador ou suas próprias chamadas.</span><span class="sxs-lookup"><span data-stu-id="114e6-155">In general, the provider is initially an administrator and alternates between **CoImpersonateClient** and **CoRevertToSelf** depending on whether it is making a call that represents the caller or its own calls.</span></span> <span data-ttu-id="114e6-156">É responsabilidade do provedor fazer essas chamadas corretamente para não expor uma brecha de segurança para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="114e6-156">It is the responsibility of the provider to place these calls correctly so as not to expose a security hole to the end user.</span></span> <span data-ttu-id="114e6-157">Por exemplo, o provedor deve chamar apenas funções nativas do Windows dentro da sequência de código representada.</span><span class="sxs-lookup"><span data-stu-id="114e6-157">For example, the provider should only call native Windows functions within the impersonated code sequence.</span></span>

> [!Note]  
> <span data-ttu-id="114e6-158">A finalidade de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) é definir a segurança de um provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-158">The purpose of [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is to set security for a provider.</span></span> <span data-ttu-id="114e6-159">Se você determinar que sua representação falhou, deverá retornar um código de conclusão apropriado para WMI por meio de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="114e6-159">If you determine that your impersonation has failed, you should return an appropriate completion code to WMI through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="114e6-160">Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](#handling-access-denied-messages-in-a-provider).</span><span class="sxs-lookup"><span data-stu-id="114e6-160">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

 

## <a name="maintaining-security-levels-in-a-provider"></a><span data-ttu-id="114e6-161">Mantendo níveis de segurança em um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-161">Maintaining Security Levels in a Provider</span></span>

<span data-ttu-id="114e6-162">Os provedores não podem chamar [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) uma vez em uma implementação de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e supõem que as credenciais de representação permaneçam em vigor durante o provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-162">Providers cannot call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) one time in an implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and assume that the impersonation credentials remain in place for the duration of the provider.</span></span> <span data-ttu-id="114e6-163">Em vez disso, chame **CoImpersonateClient** várias vezes durante o curso de uma implementação para impedir que o WMI altere as credenciais.</span><span class="sxs-lookup"><span data-stu-id="114e6-163">Instead, call **CoImpersonateClient** multiple times during the course of an implementation to keep WMI from changing the credentials.</span></span>

<span data-ttu-id="114e6-164">A principal preocupação de definir a representação de um provedor é a reentrância.</span><span class="sxs-lookup"><span data-stu-id="114e6-164">The main concern for setting impersonation for a provider is reentrancy.</span></span> <span data-ttu-id="114e6-165">Nesse contexto, a reentrância é quando um provedor faz uma chamada ao WMI para obter informações e aguarda até que o WMI chame de volta para o provedor.</span><span class="sxs-lookup"><span data-stu-id="114e6-165">In this context, reentrancy is when a provider makes a call to WMI for information and waits until WMI calls back into the provider.</span></span> <span data-ttu-id="114e6-166">Em essência, o thread de execução deixa o código do provedor, apenas para reinserir o código em uma data posterior.</span><span class="sxs-lookup"><span data-stu-id="114e6-166">In essence, the thread of execution leaves the provider code, only to reenter the code at a later date.</span></span> <span data-ttu-id="114e6-167">A reentrada faz parte do design do COM e geralmente não é uma preocupação.</span><span class="sxs-lookup"><span data-stu-id="114e6-167">Reentry is a part of the design of COM, and is generally not a concern.</span></span> <span data-ttu-id="114e6-168">No entanto, quando o thread de execução entra em WMI, o thread assume os níveis de representação do WMI.</span><span class="sxs-lookup"><span data-stu-id="114e6-168">However, when the thread of execution enters WMI, the thread takes on the impersonation levels of WMI.</span></span> <span data-ttu-id="114e6-169">Quando o thread retorna ao provedor, você deve redefinir os níveis de representação com outra chamada para [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="114e6-169">When the thread returns to the provider, you must reset the impersonation levels with another call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span>

<span data-ttu-id="114e6-170">Para se proteger de brechas de segurança em seu provedor, você deve fazer chamadas reentrantes no WMI somente ao mesmo tempo que representa o cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-170">To protect yourself from security holes in your provider, you should make reentrant calls into WMI only while impersonating the client.</span></span> <span data-ttu-id="114e6-171">Ou seja, as chamadas para o WMI devem ser feitas depois que você chamar [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e antes de chamar o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="114e6-171">That is, calls to WMI should be made after you call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and before you call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span> <span data-ttu-id="114e6-172">Como o **CoRevertToSelf** faz com que a representação seja definida para o WMI de nível de usuário em execução, em geral, as chamadas reentrante para o WMI após chamar o **CoRevertToSelf** podem fornecer ao usuário e a todos os provedores chamados, muito mais recursos do que deveriam ter.</span><span class="sxs-lookup"><span data-stu-id="114e6-172">Because **CoRevertToSelf** causes the impersonation to be set to the user level WMI is running, generally LocalSystem, reentrant calls to WMI after calling **CoRevertToSelf** could give the user, and any providers called, a lot more capabilities than they should have.</span></span>

> [!Note]  
> <span data-ttu-id="114e6-173">Se você chamar uma função do sistema ou outro método de interface, não haverá garantia de que o contexto de chamada seja mantido.</span><span class="sxs-lookup"><span data-stu-id="114e6-173">If you call a system function or another interface method, the call context is not guaranteed to be maintained.</span></span>

 

## <a name="handling-access-denied-messages-in-a-provider"></a><span data-ttu-id="114e6-174">Manipulando mensagens de acesso negado em um provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-174">Handling Access Denied Messages in a Provider</span></span>

<span data-ttu-id="114e6-175">A maioria das mensagens de erro de acesso negado aparece quando um cliente solicita uma classe ou informações às quais eles não têm acesso.</span><span class="sxs-lookup"><span data-stu-id="114e6-175">Most Access Denied error messages appear when a client requests a class or information to which they do not have access.</span></span> <span data-ttu-id="114e6-176">Se o provedor retornar uma mensagem de erro de acesso negado ao WMI e o WMI passarem por isso para o cliente, o cliente poderá inferir que as informações existem.</span><span class="sxs-lookup"><span data-stu-id="114e6-176">If the provider returns an Access Denied error message to WMI and WMI passes this on to the client, the client can infer that the information exists.</span></span> <span data-ttu-id="114e6-177">Em algumas situações, isso pode ser uma violação de segurança.</span><span class="sxs-lookup"><span data-stu-id="114e6-177">In some situations, this can be a breach of security.</span></span> <span data-ttu-id="114e6-178">Portanto, o provedor não deve propagar a mensagem para o cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-178">Therefore, your provider should not propagate the message to the client.</span></span> <span data-ttu-id="114e6-179">Em vez disso, o conjunto de classes que o provedor forneceu não deve ser exposto.</span><span class="sxs-lookup"><span data-stu-id="114e6-179">Instead, the set of classes that the provider would have supplied should not be exposed.</span></span> <span data-ttu-id="114e6-180">Da mesma forma, um provedor de instância dinâmica deve chamar a fonte de dados subjacente para determinar como lidar com mensagens de acesso negado.</span><span class="sxs-lookup"><span data-stu-id="114e6-180">Similarly, a dynamic instance provider should call to the underlying data source to determine how to deal with Access Denied messages.</span></span> <span data-ttu-id="114e6-181">É responsabilidade do provedor replicar essa filosofia no ambiente WMI.</span><span class="sxs-lookup"><span data-stu-id="114e6-181">It is the responsibility of the provider to replicate that philosophy into the WMI environment.</span></span> <span data-ttu-id="114e6-182">Para obter mais informações, consulte [relatar instâncias parciais](#reporting-partial-instances) e [relatar enumerações parciais](#reporting-partial-enumerations).</span><span class="sxs-lookup"><span data-stu-id="114e6-182">For more information, see [Reporting Partial Instances](#reporting-partial-instances) and [Reporting Partial Enumerations](#reporting-partial-enumerations).</span></span>

<span data-ttu-id="114e6-183">Ao determinar como seu provedor deve lidar com mensagens de acesso negado, você deve escrever e depurar seu código.</span><span class="sxs-lookup"><span data-stu-id="114e6-183">When you determine how your provider should handle Access Denied messages, you must write and debug your code.</span></span> <span data-ttu-id="114e6-184">Durante a depuração, geralmente é conveniente distinguir entre uma negação devido à baixa representação e a uma negação devido a um erro em seu código.</span><span class="sxs-lookup"><span data-stu-id="114e6-184">While debugging, it is often convenient to distinguish between a denial due to low impersonation, and a denial due to an error in your code.</span></span> <span data-ttu-id="114e6-185">Você pode usar um teste simples em seu código para determinar a diferença.</span><span class="sxs-lookup"><span data-stu-id="114e6-185">You can use a simple test in your code to determine the difference.</span></span> <span data-ttu-id="114e6-186">Para obter mais informações, consulte [Depurando seu código de acesso negado](#debugging-your-access-denied-code).</span><span class="sxs-lookup"><span data-stu-id="114e6-186">For more information, see [Debugging your Access Denied Code](#debugging-your-access-denied-code).</span></span>

## <a name="reporting-partial-instances"></a><span data-ttu-id="114e6-187">Relatórios de instâncias parciais</span><span class="sxs-lookup"><span data-stu-id="114e6-187">Reporting Partial Instances</span></span>

<span data-ttu-id="114e6-188">Uma ocorrência comum de uma mensagem de acesso negado é quando o WMI não pode fornecer todas as informações para preencher uma instância.</span><span class="sxs-lookup"><span data-stu-id="114e6-188">One common occurrence of an Access Denied message is when WMI cannot provide all the information to fill an instance.</span></span> <span data-ttu-id="114e6-189">Por exemplo, um cliente pode ter autoridade para exibir um objeto de unidade de disco rígido, mas pode não ter autoridade para ver quanto espaço está disponível na própria unidade de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="114e6-189">For example, a client may have the authority to view a hard disk drive object, but may not have authority to see how much space is available on the hard disk drive itself.</span></span> <span data-ttu-id="114e6-190">Seu provedor deve determinar como lidar com qualquer situação quando o provedor não puder preencher completamente uma instância com propriedades devido a uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="114e6-190">Your provider must determine how to handle any situation when the provider cannot completely fill an instance with properties due to an access violation.</span></span>

<span data-ttu-id="114e6-191">O WMI não requer uma única resposta para clientes que têm acesso parcial a uma instância.</span><span class="sxs-lookup"><span data-stu-id="114e6-191">WMI does not require a single response to clients that have partial access to an instance.</span></span> <span data-ttu-id="114e6-192">Em vez disso, o WMI versão 1. x permite ao provedor uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="114e6-192">Instead, WMI version 1.x allows the provider one of the following options:</span></span>

-   <span data-ttu-id="114e6-193">Reprovar toda a operação com **acesso de WBEM e \_ \_ \_ negado** e não retornar nenhuma instância.</span><span class="sxs-lookup"><span data-stu-id="114e6-193">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="114e6-194">Retornar um objeto de erro junto com o **WBEM \_ E \_ acesso \_ negado**, para descrever o motivo da negação.</span><span class="sxs-lookup"><span data-stu-id="114e6-194">Return an error object along with **WBEM\_E\_ACCESS\_DENIED**, to describe the reason for the denial.</span></span>

-   <span data-ttu-id="114e6-195">Retornar todas as propriedades disponíveis e preencher as propriedades não disponíveis com **NULL**.</span><span class="sxs-lookup"><span data-stu-id="114e6-195">Return all available properties, and fill unavailable properties with **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="114e6-196">Certifique-se de que o retorno de **WBEM \_ E \_ acesso \_ negado** não crie uma brecha de segurança em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="114e6-196">Make sure that returning **WBEM\_E\_ACCESS\_DENIED** does not create a security hole in your enterprise.</span></span>

 

## <a name="reporting-partial-enumerations"></a><span data-ttu-id="114e6-197">Relatando enumerações parciais</span><span class="sxs-lookup"><span data-stu-id="114e6-197">Reporting Partial Enumerations</span></span>

<span data-ttu-id="114e6-198">Outra ocorrência comum de uma violação de acesso é quando o WMI não pode retornar todas as enumerações.</span><span class="sxs-lookup"><span data-stu-id="114e6-198">Another common occurrence of an access violation is when WMI cannot return all of an enumeration.</span></span> <span data-ttu-id="114e6-199">Por exemplo, um cliente pode ter acesso para exibir todos os objetos de computador de rede local, mas pode não ter acesso para exibir objetos de computador fora do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="114e6-199">For example, a client may have access to view all of the local network computer objects, but may not have access to view computer objects outside of his domain.</span></span> <span data-ttu-id="114e6-200">Seu provedor deve determinar como lidar com qualquer situação quando uma enumeração não puder ser concluída devido a uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="114e6-200">Your provider must determine how to handle any situation when an enumeration cannot be completed due to an access violation.</span></span>

<span data-ttu-id="114e6-201">Assim como com um provedor de instância, o WMI não requer uma única resposta a uma enumeração parcial.</span><span class="sxs-lookup"><span data-stu-id="114e6-201">As with an instance provider, WMI does not require a single response to a partial enumeration.</span></span> <span data-ttu-id="114e6-202">Em vez disso, o WMI versão 1. x permite que um provedor seja uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="114e6-202">Instead, WMI version 1.x allows a provider one of the following options:</span></span>

-   <span data-ttu-id="114e6-203">Retornar **WBEM \_ S \_ sem \_ erro** para todas as instâncias que o provedor pode acessar.</span><span class="sxs-lookup"><span data-stu-id="114e6-203">Return **WBEM\_S\_NO\_ERROR** for all instances that the provider can access.</span></span>

    <span data-ttu-id="114e6-204">Se você usar essa opção, o usuário não saberá que algumas instâncias não estavam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="114e6-204">If you use this option, the user is not aware that some instances were not available.</span></span> <span data-ttu-id="114e6-205">Vários provedores, como aqueles que usam o linguagem SQL (SQL) com segurança em nível de linha, retornam resultados parciais com êxito usando o nível de segurança do chamador para definir o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="114e6-205">A number of providers, such as those using Structured Query Language (SQL) with row-level security, return successful partial results using the security level of the caller to define the result set.</span></span>

-   <span data-ttu-id="114e6-206">Reprovar toda a operação com **acesso de WBEM e \_ \_ \_ negado** e não retornar nenhuma instância.</span><span class="sxs-lookup"><span data-stu-id="114e6-206">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="114e6-207">O provedor pode opcionalmente incluir um objeto de erro que descreve a situação para o cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-207">The provider may optionally include an error object that describes the situation to the client.</span></span> <span data-ttu-id="114e6-208">Observe que alguns provedores podem acessar fontes de dados em série e podem não encontrar negações até MSRC durante por meio da enumeração.</span><span class="sxs-lookup"><span data-stu-id="114e6-208">Note that some providers may access data sources serially and may not encounter denials until partway through the enumeration.</span></span>

-   <span data-ttu-id="114e6-209">Retornar todas as instâncias que podem ser acessadas, mas também retornar o código de status não-erro **WBEM \_ \_ acesso \_ negado**.</span><span class="sxs-lookup"><span data-stu-id="114e6-209">Return all of the instances that can be accessed but also return the nonerror status code **WBEM\_S\_ACCESS\_DENIED**.</span></span>

    <span data-ttu-id="114e6-210">O provedor deve observar a negação durante a enumeração e pode continuar fornecendo instâncias, concluindo com o código de status não-erro.</span><span class="sxs-lookup"><span data-stu-id="114e6-210">The provider should note the denial during enumeration and may continue providing instances, finishing up with the nonerror status code.</span></span> <span data-ttu-id="114e6-211">O provedor também pode optar por encerrar a enumeração na primeira negação.</span><span class="sxs-lookup"><span data-stu-id="114e6-211">The provider may also elect to terminate the enumeration at the first denial.</span></span> <span data-ttu-id="114e6-212">A justificativa para essa opção é que provedores diferentes têm paradigmas de recuperação diferentes.</span><span class="sxs-lookup"><span data-stu-id="114e6-212">The justification for this option is that different providers have different retrieval paradigms.</span></span> <span data-ttu-id="114e6-213">Um provedor pode já ter entregue instâncias antes de descobrir uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="114e6-213">A provider may have already delivered instances before discovering an access violation.</span></span> <span data-ttu-id="114e6-214">Alguns provedores podem optar por continuar fornecendo outras instâncias e outras talvez queiram encerrar.</span><span class="sxs-lookup"><span data-stu-id="114e6-214">Some providers may elect to continue providing other instances and others may wish to terminate.</span></span>

<span data-ttu-id="114e6-215">Devido à estrutura de COM, não é possível realizar marshaling de todas as informações durante um erro, exceto para um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="114e6-215">Due to the structure of COM, you cannot marshal back any information during an error except for an error object.</span></span> <span data-ttu-id="114e6-216">Portanto, você não pode retornar as informações e um código de erro.</span><span class="sxs-lookup"><span data-stu-id="114e6-216">Therefore, you cannot return both information and an error code.</span></span> <span data-ttu-id="114e6-217">Se você optar por retornar informações, deverá usar um código de status de não erro.</span><span class="sxs-lookup"><span data-stu-id="114e6-217">If you choose to return information, you must use a nonerror status code instead.</span></span>

## <a name="debugging-your-access-denied-code"></a><span data-ttu-id="114e6-218">Depurando seu código de acesso negado</span><span class="sxs-lookup"><span data-stu-id="114e6-218">Debugging Your Access Denied Code</span></span>

<span data-ttu-id="114e6-219">Alguns aplicativos podem usar níveis de representação inferiores à representação de **nível de imp do RPC \_ \_ \_ \_ C**.</span><span class="sxs-lookup"><span data-stu-id="114e6-219">Some applications may use impersonation levels lower than **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span> <span data-ttu-id="114e6-220">Nesse caso, a maioria das chamadas de representação feitas pelo provedor para o aplicativo cliente falhará.</span><span class="sxs-lookup"><span data-stu-id="114e6-220">In this case, most impersonation calls made by the provider for the client application will fail.</span></span> <span data-ttu-id="114e6-221">Para projetar e implementar um provedor com êxito, você deve ter essa ideia em mente.</span><span class="sxs-lookup"><span data-stu-id="114e6-221">To successfully design and implement a provider, you must keep this idea in mind.</span></span>

<span data-ttu-id="114e6-222">Por padrão, o único outro nível de representação que pode acessar um provedor é **a \_ \_ identificação do \_ nível \_ de imp do RPC C**.</span><span class="sxs-lookup"><span data-stu-id="114e6-222">By default, the only other level of impersonation that can access a provider is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**.</span></span> <span data-ttu-id="114e6-223">Nos casos em que um aplicativo cliente usa a **identificação de nível de Imp de RPC \_ C \_ \_ \_**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) não retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="114e6-223">In cases where a client application uses **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not return an error code.</span></span> <span data-ttu-id="114e6-224">Em vez disso, o provedor representa o cliente apenas para fins de identificação.</span><span class="sxs-lookup"><span data-stu-id="114e6-224">Instead, the provider impersonates the client for identification purposes only.</span></span> <span data-ttu-id="114e6-225">Portanto, a maioria dos métodos do Windows chamados pelo provedor retornará uma mensagem de acesso negado.</span><span class="sxs-lookup"><span data-stu-id="114e6-225">Therefore, most Windows methods called by the provider will return an access denied message.</span></span> <span data-ttu-id="114e6-226">Isso é inofensivo na prática, pois os usuários não terão permissão para fazer nada inadequado.</span><span class="sxs-lookup"><span data-stu-id="114e6-226">This is harmless in practice, as users will not be permitted to do anything inappropriate.</span></span> <span data-ttu-id="114e6-227">No entanto, pode ser útil durante o desenvolvimento do provedor saber se o cliente foi realmente representado ou não.</span><span class="sxs-lookup"><span data-stu-id="114e6-227">However, it may be useful during provider development to know whether the client was truly impersonated or not.</span></span>

<span data-ttu-id="114e6-228">O código requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="114e6-228">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="114e6-229">O exemplo de código a seguir mostra como determinar se um provedor representou com êxito um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="114e6-229">The following code example shows how to determine whether a provider has successfully impersonated a client application.</span></span>


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a><span data-ttu-id="114e6-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="114e6-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="114e6-231">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="114e6-231">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="114e6-232">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="114e6-232">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="114e6-233">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="114e6-233">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
