---
description: Consumidores temporários e permanentes têm métodos diferentes para proteger a entrega de eventos.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Recebendo eventos com segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755024"
---
# <a name="receiving-events-securely"></a><span data-ttu-id="7696e-103">Recebendo eventos com segurança</span><span class="sxs-lookup"><span data-stu-id="7696e-103">Receiving Events Securely</span></span>

<span data-ttu-id="7696e-104">Consumidores temporários e permanentes têm métodos diferentes para proteger a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="7696e-104">Temporary and permanent consumers have different methods of securing event delivery.</span></span>

<span data-ttu-id="7696e-105">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="7696e-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="7696e-106">Protegendo consumidores temporários</span><span class="sxs-lookup"><span data-stu-id="7696e-106">Securing Temporary Consumers</span></span>](#securing-temporary-consumers)
-   [<span data-ttu-id="7696e-107">Protegendo consumidores permanentes</span><span class="sxs-lookup"><span data-stu-id="7696e-107">Securing Permanent Consumers</span></span>](#securing-permanent-consumers)
-   [<span data-ttu-id="7696e-108">Protegendo a assinatura permanente</span><span class="sxs-lookup"><span data-stu-id="7696e-108">Securing the Permanent Subscription</span></span>](#securing-the-permanent-subscription)
-   [<span data-ttu-id="7696e-109">Definindo um Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="7696e-109">Setting an Administrator-Only SD</span></span>](#setting-an-administrator-only-sd)
-   [<span data-ttu-id="7696e-110">Representando a identidade do provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="7696e-110">Impersonating the Event Provider Identity</span></span>](#impersonating-the-event-provider-identity)
-   [<span data-ttu-id="7696e-111">SIDs e assinaturas permanentes</span><span class="sxs-lookup"><span data-stu-id="7696e-111">SIDs and Permanent Subscriptions</span></span>](#sids-and-permanent-subscriptions)
-   [<span data-ttu-id="7696e-112">Criando assinaturas permanentes usando contas de domínio</span><span class="sxs-lookup"><span data-stu-id="7696e-112">Creating Permanent Subscriptions Using Domain Accounts</span></span>](#creating-permanent-subscriptions-using-domain-accounts)
-   [<span data-ttu-id="7696e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7696e-113">Related topics</span></span>](#related-topics)

## <a name="securing-temporary-consumers"></a><span data-ttu-id="7696e-114">Protegendo consumidores temporários</span><span class="sxs-lookup"><span data-stu-id="7696e-114">Securing Temporary Consumers</span></span>

<span data-ttu-id="7696e-115">Um [*consumidor temporário*](gloss-t.md) é executado até que o sistema seja reinicializado ou o WMI seja interrompido, mas não poderá ser iniciado se um evento específico for gerado.</span><span class="sxs-lookup"><span data-stu-id="7696e-115">A [*temporary consumers*](gloss-t.md) runs until the system is rebooted or WMI is stopped but cannot be started if a specific event is raised.</span></span> <span data-ttu-id="7696e-116">Por exemplo, uma chamada para [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) cria um consumidor temporário.</span><span class="sxs-lookup"><span data-stu-id="7696e-116">For example, a call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) creates a temporary consumer.</span></span>

<span data-ttu-id="7696e-117">As chamadas [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ou [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) criam consumidores de eventos temporários.</span><span class="sxs-lookup"><span data-stu-id="7696e-117">The calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) or [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) create temporary event consumers.</span></span> <span data-ttu-id="7696e-118">Os consumidores temporários não podem controlar quem fornece eventos para o [*coletor*](gloss-s.md) de eventos que eles criam.</span><span class="sxs-lookup"><span data-stu-id="7696e-118">Temporary consumers cannot control who provides events to the event [*sink*](gloss-s.md) they create.</span></span>

<span data-ttu-id="7696e-119">Chamadas para métodos [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) podem ser feitas de forma síncrona, [*semisynchronously*](gloss-s.md)ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7696e-119">Calls to [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) methods can be made synchronously, [*semisynchronously*](gloss-s.md), or asynchronously.</span></span> <span data-ttu-id="7696e-120">Por exemplo, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) é um método síncrono que pode ser chamado de semisynchronously, dependendo de como o parâmetro *iFlags* é definido.</span><span class="sxs-lookup"><span data-stu-id="7696e-120">For example, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) is a synchronous method that can be called semisynchronously, depending on how the *iflags* parameter is set.</span></span> <span data-ttu-id="7696e-121">[**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) é uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7696e-121">[**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) is an asynchronous call.</span></span>

<span data-ttu-id="7696e-122">Lembre-se de que o retorno de chamada para o coletor das versões assíncronas dessas chamadas pode não ser retornado no mesmo nível de autenticação que a chamada que o script fez.</span><span class="sxs-lookup"><span data-stu-id="7696e-122">Be aware that the callback to the sink for the asynchronous versions of these calls might not be returned at the same authentication level as the call the script made.</span></span> <span data-ttu-id="7696e-123">Portanto, é recomendável que você use semisynchronous em vez de chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="7696e-123">Therefore, it is recommended that you use semisynchronous instead of asynchronous calls.</span></span> <span data-ttu-id="7696e-124">Se você precisar de comunicação assíncrona, consulte [chamar um método](calling-a-method.md) e [definir a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-124">If you require asynchronous communication, see [Calling a Method](calling-a-method.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="7696e-125">Os assinantes de script não podem verificar os direitos de acesso de um provedor de eventos para fornecer eventos ao coletor criado pelo script.</span><span class="sxs-lookup"><span data-stu-id="7696e-125">Scripting subscribers cannot check the access rights of an event provider to provide events to the sink created by the script.</span></span> <span data-ttu-id="7696e-126">Portanto, é recomendável que as chamadas para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usem o formulário semisynchronous da chamada e usem configurações de segurança específicas.</span><span class="sxs-lookup"><span data-stu-id="7696e-126">Therefore, it is recommended that calls to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) use the semisynchronous form of the call and use specific security settings.</span></span> <span data-ttu-id="7696e-127">Para obter mais informações, consulte [fazendo uma chamada de Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-127">For more information, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="securing-permanent-consumers"></a><span data-ttu-id="7696e-128">Protegendo consumidores permanentes</span><span class="sxs-lookup"><span data-stu-id="7696e-128">Securing Permanent Consumers</span></span>

<span data-ttu-id="7696e-129">Um [*consumidor permanente*](gloss-p.md) tem uma assinatura permanente para eventos de um provedor de eventos que persistirá depois que o sistema operacional for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="7696e-129">A [*permanent consumers*](gloss-p.md) has a permanent subscription to events from an event provider that will persist after the operating system is restarted.</span></span> <span data-ttu-id="7696e-130">Um provedor de eventos que dá suporte a consumidores permanentes é um [*provedor de consumidor de eventos*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-130">An event provider that supports permanent consumers is a [*event consumer provider*](gloss-e.md).</span></span> <span data-ttu-id="7696e-131">Se o provedor de eventos não estiver em execução quando um evento ocorrer, o WMI iniciará o provedor quando precisar entregar eventos.</span><span class="sxs-lookup"><span data-stu-id="7696e-131">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span> <span data-ttu-id="7696e-132">O WMI identifica a qual provedor de consumidor os eventos devem ser entregues, com base na instância [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que associa a instância [**\_ \_ Win32Provider**](--win32provider.md) do provedor de consumidor a uma [*classe de consumidor lógica*](gloss-l.md) definida pelo provedor de consumidor.</span><span class="sxs-lookup"><span data-stu-id="7696e-132">WMI identifies which consumer provider the events should be delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a [*logical consumer class*](gloss-l.md) defined by the consumer provider.</span></span> <span data-ttu-id="7696e-133">Para obter mais informações sobre a função de provedores de consumidor, consulte [escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-133">For more information about the role of consumer providers, see [Writing an Event Consumer Provider](writing-an-event-consumer-provider.md).</span></span>

<span data-ttu-id="7696e-134">Os consumidores permanentes podem controlar quem envia eventos e provedores de eventos podem controlar quem acessa seus eventos.</span><span class="sxs-lookup"><span data-stu-id="7696e-134">Permanent consumers can control who sends them events and event providers can control who accesses their events.</span></span>

<span data-ttu-id="7696e-135">Scripts e aplicativos de cliente criam instâncias da classe de consumidor lógica como parte de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7696e-135">Client scripts and applications create instances of the logical consumer class as part of a subscription.</span></span> <span data-ttu-id="7696e-136">A classe consumidor lógico define quais informações o evento contém, o que o cliente pode fazer com o evento e como o evento é entregue.</span><span class="sxs-lookup"><span data-stu-id="7696e-136">The logical consumer class defines what information the event contains, what the client can do with the event, and how the event is delivered.</span></span>

<span data-ttu-id="7696e-137">As [classes de consumidor padrão](standard-consumer-classes.md) do WMI fornecem exemplos da função de classes de consumidor lógicas.</span><span class="sxs-lookup"><span data-stu-id="7696e-137">The WMI [Standard Consumer Classes](standard-consumer-classes.md) provide examples of the role of logical consumer classes.</span></span> <span data-ttu-id="7696e-138">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-138">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="securing-the-permanent-subscription"></a><span data-ttu-id="7696e-139">Protegendo a assinatura permanente</span><span class="sxs-lookup"><span data-stu-id="7696e-139">Securing the Permanent Subscription</span></span>

<span data-ttu-id="7696e-140">As assinaturas permanentes têm maior potencial para causar problemas de segurança no WMI e, portanto, têm os seguintes requisitos de segurança:</span><span class="sxs-lookup"><span data-stu-id="7696e-140">Permanent subscriptions have greater potential to cause security problems in WMI and therefore have the following security requirements:</span></span>

-   <span data-ttu-id="7696e-141">A instância de consumidor lógico, [**\_ \_ EventFilter**](--eventfilter.md), e as instâncias de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) devem ter o mesmo SID (identificador de segurança individual) na propriedade **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="7696e-141">The logical consumer instance, the [**\_\_EventFilter**](--eventfilter.md), and the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instances must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="7696e-142">Para obter mais informações, consulte [mantendo o mesmo SID em todas as instâncias de uma assinatura permanente](#sids-and-permanent-subscriptions).</span><span class="sxs-lookup"><span data-stu-id="7696e-142">For more information, see [Keeping the same SID in all instances of a permanent subscription](#sids-and-permanent-subscriptions).</span></span>
-   <span data-ttu-id="7696e-143">A conta que cria a assinatura deve ser uma conta de domínio com privilégios de administrador local ou a conta de grupo de administradores locais.</span><span class="sxs-lookup"><span data-stu-id="7696e-143">The account that creates the subscription must be either a domain account with local administrator privileges or the local Administrators group account.</span></span> <span data-ttu-id="7696e-144">Usar o SID do grupo Administradores permite que a assinatura continue a funcionar no computador local, mesmo se ela estiver desconectada da rede.</span><span class="sxs-lookup"><span data-stu-id="7696e-144">Using the Administrators group SID allows the subscription to continue to work on the local computer, even if it is disconnected from the network.</span></span> <span data-ttu-id="7696e-145">O uso de uma conta de domínio permite a identificação exata do usuário.</span><span class="sxs-lookup"><span data-stu-id="7696e-145">Using a domain account allows exact identification of the user.</span></span>

    <span data-ttu-id="7696e-146">No entanto, se o computador não estiver conectado e a criação da conta for uma conta de domínio, o consumidor falhará porque o WMI não pode verificar a identidade da conta.</span><span class="sxs-lookup"><span data-stu-id="7696e-146">However, if the computer is not connected and the creating account is a domain account, the consumer fails because WMI cannot verify the identity of the account.</span></span> <span data-ttu-id="7696e-147">Para evitar a falha de assinatura se o computador estiver desconectado da rede, use o SID do grupo Administradores para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7696e-147">To avoid subscription failure if the computer is disconnected from the network, use the Administrators group SID for a subscription.</span></span> <span data-ttu-id="7696e-148">Nesse caso, você deve garantir que a conta LocalSystem possa acessar os dados de associação de grupo no domínio.</span><span class="sxs-lookup"><span data-stu-id="7696e-148">In this case, you should ensure that the LocalSystem account can access group membership data on the domain.</span></span> <span data-ttu-id="7696e-149">Alguns provedores de consumidor de eventos têm requisitos de segurança particularmente altos, uma vez que uma assinatura não autorizada pode causar grandes danos.</span><span class="sxs-lookup"><span data-stu-id="7696e-149">Some event consumer providers have particularly high security requirements, since a rogue subscription can cause great damage.</span></span> <span data-ttu-id="7696e-150">Os exemplos são os consumidores padrão, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-150">Examples are the standard consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>

-   <span data-ttu-id="7696e-151">Você pode configurar a assinatura permanente para aceitar apenas eventos de identidades específicas do provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7696e-151">You can configure the permanent subscription to only accept events from specific event provider identities.</span></span> <span data-ttu-id="7696e-152">Defina o descritor de segurança na propriedade **EventAccess** da instância [**\_ \_ EventFilter**](--eventfilter.md) para as identidades do provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7696e-152">Set the security descriptor in the **EventAccess** property of the [**\_\_EventFilter**](--eventfilter.md) instance to the event provider identities.</span></span> <span data-ttu-id="7696e-153">O WMI compara a identidade do provedor de eventos com o descritor de segurança para determinar se o provedor tem acesso de **\_ \_ publicação de WBEM direito** .</span><span class="sxs-lookup"><span data-stu-id="7696e-153">WMI compares the identity of the event provider to the security descriptor to determine if the provider has **WBEM\_RIGHT\_PUBLISH** access.</span></span> <span data-ttu-id="7696e-154">Para obter mais informações, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-154">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

    <span data-ttu-id="7696e-155">Se o filtro permitir acesso à identidade do provedor de eventos, ele também confiará no evento.</span><span class="sxs-lookup"><span data-stu-id="7696e-155">If the filter allows access to the event provider identity, then it also trusts the event.</span></span> <span data-ttu-id="7696e-156">Isso permite que o consumidor que recebeu o evento gere um evento delegado.</span><span class="sxs-lookup"><span data-stu-id="7696e-156">This allows the consumer that received the event to raise a delegated event.</span></span>

    <span data-ttu-id="7696e-157">**Observação**  O padrão para o descritor de segurança em **EventAccess** é **nulo**, o que permite o acesso a todos.</span><span class="sxs-lookup"><span data-stu-id="7696e-157">**Note**  The default for the security descriptor in **EventAccess** is **NULL**, which allows access to everyone.</span></span> <span data-ttu-id="7696e-158">É recomendável limitar o acesso na instância de assinatura do [**\_ \_ EventFilter**](--eventfilter.md) para melhorar a segurança do evento.</span><span class="sxs-lookup"><span data-stu-id="7696e-158">Limiting access in the subscription instance of [**\_\_EventFilter**](--eventfilter.md) is recommended for better event security.</span></span>

## <a name="setting-an-administrator-only-sd"></a><span data-ttu-id="7696e-159">Definindo um Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="7696e-159">Setting an Administrator-Only SD</span></span>

<span data-ttu-id="7696e-160">O exemplo de código C++ a seguir cria um descritor de segurança somente de administrador na instância [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="7696e-160">The following C++ code example creates an administrator-only security descriptor on the [**\_\_EventFilter**](--eventfilter.md) instance.</span></span> <span data-ttu-id="7696e-161">Este exemplo cria o descritor de segurança usando SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).</span><span class="sxs-lookup"><span data-stu-id="7696e-161">This example creates the security descriptor using [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="7696e-162">Para obter mais informações sobre a **\_ \_ assinatura do WBEM direito**, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-162">For more information about **WBEM\_RIGHT\_SUBSCRIBE**, see [WMI Security Constants](wmi-security-constants.md).</span></span>


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



<span data-ttu-id="7696e-163">O exemplo de código anterior requer a seguinte referência e as \# instruções include.</span><span class="sxs-lookup"><span data-stu-id="7696e-163">The previous code example requires the following reference and \#include statements.</span></span>


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a><span data-ttu-id="7696e-164">Representando a identidade do provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="7696e-164">Impersonating the Event Provider Identity</span></span>

<span data-ttu-id="7696e-165">Um consumidor permanente pode precisar representar o provedor de eventos para processar o evento.</span><span class="sxs-lookup"><span data-stu-id="7696e-165">A permanent consumer may need to impersonate the event provider to process the event.</span></span> <span data-ttu-id="7696e-166">Os consumidores permanentes só podem representar o provedor de eventos quando existem as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="7696e-166">Permanent consumers can only impersonate the event provider when the following conditions exist:</span></span>

-   <span data-ttu-id="7696e-167">A instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) tem a propriedade **MaintainSecurityContext** definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="7696e-167">The instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) has the **MaintainSecurityContext** property set to **True**.</span></span>
-   <span data-ttu-id="7696e-168">Um evento é entregue no mesmo contexto de segurança em que o provedor estava quando gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="7696e-168">An event is delivered in the same security context that the provider was in when it generated the event.</span></span> <span data-ttu-id="7696e-169">Apenas um consumidor implementado como uma DLL, um consumidor em processo, pode receber eventos no contexto de segurança do provedor.</span><span class="sxs-lookup"><span data-stu-id="7696e-169">Only a consumer implemented as a DLL, an in-process consumer, can receive events in the security context of the provider.</span></span> <span data-ttu-id="7696e-170">Para obter mais informações sobre segurança de provedores em processo e consumidores, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="7696e-170">For more information about security of in-process providers and consumers, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="7696e-171">O provedor de eventos está sendo executado em um processo que permite a representação.</span><span class="sxs-lookup"><span data-stu-id="7696e-171">The event provider is running in a process that allows impersonation.</span></span>

<span data-ttu-id="7696e-172">A conta que executa o processo do consumidor deve ter acesso de **\_ gravação total** ao repositório do WMI (também conhecido como repositório CIM).</span><span class="sxs-lookup"><span data-stu-id="7696e-172">The account running the consumer process must have **FULL\_WRITE** access to the WMI repository (also known as the CIM repository).</span></span> <span data-ttu-id="7696e-173">Na assinatura, as instâncias [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de Sid (identificador de segurança individual) na propriedade **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="7696e-173">In the subscription, the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) instances must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="7696e-174">O WMI armazena o SID no **CreatorSID** para cada instância.</span><span class="sxs-lookup"><span data-stu-id="7696e-174">WMI stores the SID in the **CreatorSID** for each instance.</span></span>

## <a name="sids-and-permanent-subscriptions"></a><span data-ttu-id="7696e-175">SIDs e assinaturas permanentes</span><span class="sxs-lookup"><span data-stu-id="7696e-175">SIDs and Permanent Subscriptions</span></span>

<span data-ttu-id="7696e-176">Uma assinatura permanente não funciona quando a associação, o consumidor e o filtro não são criados pelo mesmo usuário, o que significa que [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de Sid (identificador de segurança individual) na propriedade **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="7696e-176">A permanent subscription does not work when the binding, the consumer, and the filter are not created by the same user, which means that the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="7696e-177">Instrumentação de Gerenciamento do Windows (WMI) armazena esse valor.</span><span class="sxs-lookup"><span data-stu-id="7696e-177">Windows Management Instrumentation (WMI) stores this value.</span></span>

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a><span data-ttu-id="7696e-178">Criando assinaturas permanentes usando contas de domínio</span><span class="sxs-lookup"><span data-stu-id="7696e-178">Creating Permanent Subscriptions Using Domain Accounts</span></span>

<span data-ttu-id="7696e-179">Vários problemas devem ser considerados ao usar contas de domínio para criar assinaturas permanentes.</span><span class="sxs-lookup"><span data-stu-id="7696e-179">Several issues must be considered when using domain accounts to create permanent subscriptions.</span></span> <span data-ttu-id="7696e-180">Cada assinatura permanente ainda deve funcionar quando nenhum usuário está conectado, o que significa que elas funcionam sob a conta LocalSystem interna.</span><span class="sxs-lookup"><span data-stu-id="7696e-180">Every permanent subscription should still work when no user is logged on, which means they function under the built-in LocalSystem account.</span></span>

<span data-ttu-id="7696e-181">Se um usuário de domínio for o criador de uma assinatura permanente para consumidores sensíveis à segurança ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), o WMI verificará se a propriedade **CreatorSID** da classe [**\_ \_ EventFilter**](--eventfilter.md) , a classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) e as instâncias do consumidor pertencem a um usuário que é membro do grupo Administradores local.</span><span class="sxs-lookup"><span data-stu-id="7696e-181">If a domain user is the creator of a permanent subscription for security sensitive consumers ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), then WMI verifies whether the **CreatorSID** property of the [**\_\_EventFilter**](--eventfilter.md) class, [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class, and the consumer instances belong to a user who is member of local Administrators group.</span></span>

<span data-ttu-id="7696e-182">O exemplo de código a seguir mostra como você pode especificar a propriedade **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="7696e-182">The following code example shows how you can specify the **CreatorSID** property.</span></span>

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

<span data-ttu-id="7696e-183">Para situações entre domínios, adicione usuários autenticados ao "grupo de acesso de autorização do Windows".</span><span class="sxs-lookup"><span data-stu-id="7696e-183">For cross domain situations, add Authenticated Users to the "Windows Authorization Access Group".</span></span>

## <a name="related-topics"></a><span data-ttu-id="7696e-184">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7696e-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7696e-185">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="7696e-185">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> <dt>

[<span data-ttu-id="7696e-186">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="7696e-186">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
