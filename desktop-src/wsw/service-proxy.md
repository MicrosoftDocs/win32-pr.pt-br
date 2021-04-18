---
title: Proxy de serviço
description: Um proxy de serviço é o proxy do lado do cliente para um serviço.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Serviços Web de proxy de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105784042"
---
# <a name="service-proxy"></a><span data-ttu-id="626c0-106">Proxy de serviço</span><span class="sxs-lookup"><span data-stu-id="626c0-106">Service Proxy</span></span>

<span data-ttu-id="626c0-107">Um proxy de serviço é o proxy do lado do cliente para um serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="626c0-108">O proxy de serviço permite que os aplicativos enviem e recebam [mensagens](message.md) por um [canal](channel.md) como chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="626c0-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="626c0-109">Os proxies de serviço são criados conforme necessário, abertos, usados para chamar um serviço e fechados quando não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="626c0-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="626c0-110">Como alternativa, um aplicativo pode reutilizar um proxy de serviço para se conectar repetidamente ao mesmo serviço sem a despesa de tempo e os recursos necessários para initialising um proxy de serviço mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="626c0-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="626c0-111">O diagrama a seguir ilustra o fluxo dos possíveis Estados do proxy de serviço e as chamadas de função ou os eventos que levam de um estado para outro.</span><span class="sxs-lookup"><span data-stu-id="626c0-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Diagrama mostrando os Estados de proxy de serviço e as chamadas de função ou eventos que levam de um estado para outro.](images/serviceproxystates.png)

<span data-ttu-id="626c0-113">Esses Estados de proxy de serviço são enumerados na enumeração de [**\_ estado do \_ proxy \_ de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="626c0-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="626c0-114">Como o diagrama anterior e o código a seguir ilustram, um proxy de serviço é criado por uma chamada para a função [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="626c0-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="626c0-115">Como parâmetros para essa chamada, WWSAPI fornece as seguintes enumerações:</span><span class="sxs-lookup"><span data-stu-id="626c0-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="626c0-116">**\_tipo de canal do WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="626c0-117">**Associação de WS \_ Channel \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="626c0-118">Ele também aceita parâmetros opcionais usando os seguintes tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="626c0-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="626c0-119">**\_ID da \_ Propriedade do proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="626c0-120">**\_Descrição da segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="626c0-121">Quando o proxy de serviço é criado, a função **WsCreateServiceProxy** retorna uma referência ao proxy de serviço, [o \_ \_ proxy de serviço WS](ws-service-proxy.md), por meio de um parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="626c0-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="626c0-122">Quando o proxy de serviço tiver sido criado, o aplicativo poderá abrir o proxy de serviço para comunicação com um serviço chamando a função [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , passando uma estrutura de [**endereço**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contém o endereço de rede do ponto de extremidade de serviço ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="626c0-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="626c0-123">Quando o proxy de serviço é aberto, o aplicativo pode usá-lo para fazer chamadas para o serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="626c0-124">Quando o aplicativo não precisar mais do proxy de serviço, ele fechará o proxy de serviço chamando a função [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="626c0-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="626c0-125">Ele também libera a memória associada chamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="626c0-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="626c0-126">Reutilizando o proxy de serviço</span><span class="sxs-lookup"><span data-stu-id="626c0-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="626c0-127">Como alternativa, depois de chamar [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , um aplicativo pode reutilizar o proxy de serviço chamando a função [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="626c0-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="626c0-128">Para obter mais informações sobre como os proxies de serviço são usados em diferentes contextos, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="626c0-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="626c0-129">Proxy de serviço e sessões</span><span class="sxs-lookup"><span data-stu-id="626c0-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="626c0-130">Operação de serviço</span><span class="sxs-lookup"><span data-stu-id="626c0-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="626c0-131">Operações de serviço no lado do cliente</span><span class="sxs-lookup"><span data-stu-id="626c0-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="626c0-132">HttpCalculatorClientExample</span><span class="sxs-lookup"><span data-stu-id="626c0-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="626c0-133">Segurança</span><span class="sxs-lookup"><span data-stu-id="626c0-133">Security</span></span>

<span data-ttu-id="626c0-134">As considerações de design de aplicativo a seguir devem ser cuidadosamente observadas quando você usa a API de proxy do serviço WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="626c0-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="626c0-135">O proxy de serviço não executará nenhuma validação dos dados além da validação básica do perfil 2,0 e da serialização XML.</span><span class="sxs-lookup"><span data-stu-id="626c0-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="626c0-136">É responsabilidade do aplicativo validar os dados contidos nos parâmetros que recebe de volta como parte da chamada.</span><span class="sxs-lookup"><span data-stu-id="626c0-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="626c0-137">Configurando o número máximo de chamadas pendentes no proxy de serviço, usando o valor de enumeração [**WS \_ proxy \_ Property \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) **\_ unproxy WS \_ \_ Max \_ Pending \_**, fornece proteção contra um servidor em execução lenta.</span><span class="sxs-lookup"><span data-stu-id="626c0-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="626c0-138">O máximo padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="626c0-138">The default maximum is 100.</span></span> <span data-ttu-id="626c0-139">Os aplicativos devem ter cuidado ao modificar os padrões.</span><span class="sxs-lookup"><span data-stu-id="626c0-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="626c0-140">O proxy de serviço não fornece nenhuma garantia de segurança além daquelas especificadas na estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usada para se comunicar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="626c0-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="626c0-141">Tome cuidado ao modificar os padrões de [mensagem](message.md) e [canal](channel.md) no proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="626c0-142">Leia as considerações de segurança associadas a mensagens e canais antes de modificar qualquer uma das propriedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="626c0-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="626c0-143">O proxy de serviço criptografa todas as credenciais que ele mantém na memória.</span><span class="sxs-lookup"><span data-stu-id="626c0-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="626c0-144">Os elementos da API a seguir estão relacionados a proxies de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="626c0-145">Callback</span><span class="sxs-lookup"><span data-stu-id="626c0-145">Callback</span></span>                                                          | <span data-ttu-id="626c0-146">Description</span><span class="sxs-lookup"><span data-stu-id="626c0-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="626c0-147">**\_retorno de \_ chamada de mensagem de proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="626c0-148">Chamado quando os cabeçalhos da mensagem de entrada estão prestes a ser enviados por ou quando um cabeçalho de mensagem de saída é apenas recebido.</span><span class="sxs-lookup"><span data-stu-id="626c0-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="626c0-149">Enumeração</span><span class="sxs-lookup"><span data-stu-id="626c0-149">Enumeration</span></span>                                                 | <span data-ttu-id="626c0-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="626c0-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="626c0-151">**\_ID da \_ propriedade da chamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="626c0-152">Enumera parâmetros opcionais para configurar uma chamada em uma operação de serviço no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="626c0-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="626c0-153">**\_ID da \_ Propriedade do proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="626c0-154">Enumera parâmetros opcionais para configurar o proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="626c0-155">**\_estado do \_ proxy de serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="626c0-156">O estado do proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="626c0-157">Função</span><span class="sxs-lookup"><span data-stu-id="626c0-157">Function</span></span>                                                       | <span data-ttu-id="626c0-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="626c0-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="626c0-159">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="626c0-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="626c0-160">Abandona uma chamada especificada em um proxy de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="626c0-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="626c0-161">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="626c0-162">Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="626c0-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="626c0-163">**WsCall**</span><span class="sxs-lookup"><span data-stu-id="626c0-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="626c0-164">Somente interno.</span><span class="sxs-lookup"><span data-stu-id="626c0-164">Internal only.</span></span> <span data-ttu-id="626c0-165">Serializa os argumentos em uma mensagem e os envia pelo canal.</span><span class="sxs-lookup"><span data-stu-id="626c0-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="626c0-166">**WsCloseServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="626c0-167">Fecha um proxy de serviço para comunicação.</span><span class="sxs-lookup"><span data-stu-id="626c0-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="626c0-168">**WsCreateServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="626c0-169">Cria um proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="626c0-170">**WsFreeServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="626c0-171">Libera a memória associada a um proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="626c0-172">**WsGetServiceProxyProperty**</span><span class="sxs-lookup"><span data-stu-id="626c0-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="626c0-173">Recupera uma propriedade de proxy de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="626c0-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="626c0-174">**WsOpenServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="626c0-175">Abre um proxy de serviço para um ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="626c0-176">**WsResetServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="626c0-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="626c0-177">Redefine o proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="626c0-178">Handle</span><span class="sxs-lookup"><span data-stu-id="626c0-178">Handle</span></span>                                     | <span data-ttu-id="626c0-179">Description</span><span class="sxs-lookup"><span data-stu-id="626c0-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="626c0-180">\_proxy de serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="626c0-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="626c0-181">Um tipo opaco usado para fazer referência a um proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="626c0-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="626c0-182">Estrutura</span><span class="sxs-lookup"><span data-stu-id="626c0-182">Structure</span></span>                                         | <span data-ttu-id="626c0-183">Description</span><span class="sxs-lookup"><span data-stu-id="626c0-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="626c0-184">**\_propriedade de chamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="626c0-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="626c0-185">Especifica uma propriedade de chamada.</span><span class="sxs-lookup"><span data-stu-id="626c0-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="626c0-186">[**WS \_ \_propriedade de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="626c0-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="626c0-187">Especifica uma propriedade de proxy.</span><span class="sxs-lookup"><span data-stu-id="626c0-187">Specifies a proxy property.</span></span> |



 

 

 




