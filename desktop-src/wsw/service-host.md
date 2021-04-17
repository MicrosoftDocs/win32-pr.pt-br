---
title: Host de serviço
description: O host de serviço é o ambiente de tempo de execução para hospedar um serviço em um processo.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Serviços Web do host de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105784653"
---
# <a name="service-host"></a><span data-ttu-id="8dd36-106">Host de serviço</span><span class="sxs-lookup"><span data-stu-id="8dd36-106">Service Host</span></span>

<span data-ttu-id="8dd36-107">O host de serviço é o ambiente de tempo de execução para hospedar um serviço em um processo.</span><span class="sxs-lookup"><span data-stu-id="8dd36-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="8dd36-108">Um serviço pode configurar um ou mais pontos de extremidade dentro de um host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-108">A service can configure one or more endpoints inside a service host.</span></span>

![Diagrama que mostra a estrutura de um host de serviço que contém um ponto de extremidade de serviço.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="8dd36-110">Criando um host de serviço</span><span class="sxs-lookup"><span data-stu-id="8dd36-110">Creating a service host</span></span>

<span data-ttu-id="8dd36-111">Antes de criar um host de serviço, um serviço precisa definir seus pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="8dd36-112">Um ponto de extremidade no host de serviço é especificado na estrutura de [**\_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) e é definido pelas seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="8dd36-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="8dd36-113">Um endereço, que é o URI físico no qual o serviço será hospedado.</span><span class="sxs-lookup"><span data-stu-id="8dd36-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="8dd36-114">Uma estrutura de [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que especifica o tipo do canal subjacente para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="8dd36-115">Uma estrutura de [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) que especifica a associação do canal.</span><span class="sxs-lookup"><span data-stu-id="8dd36-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="8dd36-116">Uma estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contém a descrição de segurança para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="8dd36-117">Uma estrutura de [**\_ \_ contrato de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) que representa o [contrato de serviço](contract.md) para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="8dd36-118">Uma estrutura de [**retorno de chamada do WS \_ Service \_ Security \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) que especifica uma função de retorno de chamada de autorização para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="8dd36-119">Uma estrutura de [**\_ propriedade de ponto de \_ extremidade \_ de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) que contém uma matriz de propriedades de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="8dd36-120">Somente contratos unidirecionais têm suporte para SOAP sobre UDP, representado pela [**\_ Associação de \_ canal \_ do WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) na enumeração de **associação do WS \_ Channel \_** .</span><span class="sxs-lookup"><span data-stu-id="8dd36-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="8dd36-121">Depois que um ponto de extremidade é definido, ele pode ser passado para a função [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , que usa uma matriz de ponteiros para estruturas de [**ponto de \_ \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .</span><span class="sxs-lookup"><span data-stu-id="8dd36-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="8dd36-122">Um aplicativo pode, opcionalmente, fornecer uma matriz de [**Propriedades de serviço**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) para [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) para definir configurações personalizadas no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="8dd36-123">Um aplicativo abre o host de serviço para iniciar a aceitação de solicitações de cliente.</span><span class="sxs-lookup"><span data-stu-id="8dd36-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="8dd36-124">Depois de abrir o host de serviço, o aplicativo poderá fechá-lo se não houver mais operações que o exijam.</span><span class="sxs-lookup"><span data-stu-id="8dd36-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="8dd36-125">Observe que isso não libera seus recursos e que pode ser reaberto com uma chamada subsequente para [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span><span class="sxs-lookup"><span data-stu-id="8dd36-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="8dd36-126">Depois de fechar o host de serviço, um aplicativo pode redefinir o host de serviço para reutilização.</span><span class="sxs-lookup"><span data-stu-id="8dd36-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="8dd36-127">Quando o aplicativo é feito com o host de serviço, ele pode liberar os recursos associados ao host de serviço chamando a função [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) .</span><span class="sxs-lookup"><span data-stu-id="8dd36-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="8dd36-128">Observe que [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) deve ser chamado antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="8dd36-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="8dd36-129">Para obter informações sobre como anexar um estado personalizado ao host de serviço, consulte [estado do host do usuário](user-host-state.md)</span><span class="sxs-lookup"><span data-stu-id="8dd36-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="8dd36-130">Para obter informações sobre autorização em um host de serviço para um determinado ponto de extremidade, consulte [autorização de serviço](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="8dd36-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="8dd36-131">Para Iinformation sobre como implementar operações de serviço e contratos de serviço para um serviço, consulte os tópicos [operações de serviço](server-side-service-operations.md) e [contrato de serviço](contract.md).</span><span class="sxs-lookup"><span data-stu-id="8dd36-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="8dd36-132">Segurança</span><span class="sxs-lookup"><span data-stu-id="8dd36-132">Security</span></span>

<span data-ttu-id="8dd36-133">Um aplicativo pode usar as propriedades de acompanhamento para controlar a quantidade de recursos alocados pelo host de serviço em nome do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="8dd36-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="8dd36-134">[**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ máximo \_ aceitando \_ canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="8dd36-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="8dd36-135">[**WS \_ Propriedade de ponto de extremidade de serviço- \_ \_ \_ \_ simultaneidade máxima**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="8dd36-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="8dd36-136">[**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ máximo de \_ \_ canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="8dd36-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="8dd36-137">[**WS \_ \_ \_ \_ \_ \_ \_ tamanho máximo do heap de corpo da propriedade de ponto de extremidade de serviço**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="8dd36-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="8dd36-138">[**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ tamanho máximo do \_ \_ pool \_ de chamadas**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="8dd36-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="8dd36-139">[**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ tamanho máximo do \_ \_ pool \_ de canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span><span class="sxs-lookup"><span data-stu-id="8dd36-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="8dd36-140">Os padrões seguros são escolhidos para cada uma dessas propriedades, um aplicativo deve ser cuidadoso se quiser modificar essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dd36-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="8dd36-141">Além das propriedades mencionadas acima, as propriedades de [canal](channel.md), de [ouvinte](listener.md) e de [mensagem](message.md) específicas também podem ser modificadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8dd36-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="8dd36-142">Consulte as considerações de segurança desses componentes antes de modificar qualquer uma dessas configurações.</span><span class="sxs-lookup"><span data-stu-id="8dd36-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="8dd36-143">Além disso, as seguintes considerações de design de aplicativo devem ser avaliadas cuidadosamente ao usar a API de host do serviço WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="8dd36-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="8dd36-144">Ao usar MEX, os aplicativos devem ter cuidado para não divulgar dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="8dd36-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="8dd36-145">Como uma mitigação, se a natureza dos dados expostos por meio de MEX for confidencial, os aplicativos poderão optar por configurar o ponto de extremidade MEX com uma associação segura que exija autenticação no mínimo e implementar a autorização como parte do ponto de extremidade usando o [**retorno de chamada de \_ segurança do serviço \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="8dd36-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="8dd36-146">Por padrão, as informações de erro avançadas por meio de falhas estão desabilitadas no host de serviço pela propriedade de [**divulgação de falha de \_ Propriedade do serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="8dd36-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="8dd36-147">É mediante a vontade do aplicativo enviar informações de erro avançadas como parte da falha.</span><span class="sxs-lookup"><span data-stu-id="8dd36-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="8dd36-148">No entanto, isso pode resultar em divulgação de informações e, portanto, é recomendável que essa configuração seja alterada apenas para cenários de depuração.</span><span class="sxs-lookup"><span data-stu-id="8dd36-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="8dd36-149">Além da validação executada para o perfil básico 2,0 e a serialização XML, o host de serviço não executa nenhuma validação no conteúdo de dados recebido como parte dos parâmetros de operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="8dd36-150">É responsabilidade do aplicativo executar todas as validações de parâmetro por conta própria.</span><span class="sxs-lookup"><span data-stu-id="8dd36-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="8dd36-151">A autorização não é implementada como parte do host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="8dd36-152">No entanto, os aplicativos podem implementar seu próprio esquema de autorização usando a [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e o retorno de [**\_ \_ \_ chamada de segurança do serviço WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="8dd36-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="8dd36-153">É responsabilidade do aplicativo usar associações seguras em seu ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="8dd36-154">O host de serviço não fornece nenhuma segurança além do que está configurado no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="8dd36-155">Os seguintes elementos de API são usados com o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="8dd36-156">Callback</span><span class="sxs-lookup"><span data-stu-id="8dd36-156">Callback</span></span>                                                                             | <span data-ttu-id="8dd36-157">Description</span><span class="sxs-lookup"><span data-stu-id="8dd36-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="8dd36-158">**\_retorno de \_ chamada de canal de aceitação de serviço WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="8dd36-159">Chamado quando um canal é aceito em um ouvinte de ponto de extremidade pelo host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="8dd36-160">**\_retorno de \_ chamada de canal de fechamento de serviço WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="8dd36-161">Chamado quando um canal é fechado ou anulado em um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="8dd36-162">Enumeração</span><span class="sxs-lookup"><span data-stu-id="8dd36-162">Enumeration</span></span>                                                                    | <span data-ttu-id="8dd36-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dd36-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dd36-164">**ID da Propriedade do ponto de extremidade do \_ serviço WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="8dd36-165">Parâmetros opcionais para configurar [**um \_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="8dd36-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="8dd36-166">**\_estado do \_ host de serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="8dd36-167">Os Estados em que um host de serviço pode estar.</span><span class="sxs-lookup"><span data-stu-id="8dd36-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="8dd36-168">**\_ID da \_ Propriedade do serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="8dd36-169">Parâmetros opcionais para configurar o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="8dd36-170">Função</span><span class="sxs-lookup"><span data-stu-id="8dd36-170">Function</span></span>                                                     | <span data-ttu-id="8dd36-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dd36-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dd36-172">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="8dd36-173">Interrompe e descontinua as operações atuais no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="8dd36-174">**WsCloseServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="8dd36-175">Fecha todos os ouvintes para que nenhum novo canal seja aceito do cliente.</span><span class="sxs-lookup"><span data-stu-id="8dd36-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="8dd36-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="8dd36-177">Cria um host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="8dd36-178">**WsFreeServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="8dd36-179">Libera a memória associada a um objeto de host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="8dd36-180">**WsGetServiceHostProperty**</span><span class="sxs-lookup"><span data-stu-id="8dd36-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="8dd36-181">Recupera uma propriedade de host de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="8dd36-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="8dd36-182">**WsOpenServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="8dd36-183">Abre um host de serviço para comunicação e inicia os ouvintes em todos os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8dd36-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="8dd36-184">**WsResetServiceHost**</span><span class="sxs-lookup"><span data-stu-id="8dd36-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="8dd36-185">Redefine o host de serviço para reutilização e redefine o canal subjacente e os ouvintes para reutilização.</span><span class="sxs-lookup"><span data-stu-id="8dd36-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="8dd36-186">Handle</span><span class="sxs-lookup"><span data-stu-id="8dd36-186">Handle</span></span>                                       | <span data-ttu-id="8dd36-187">Description</span><span class="sxs-lookup"><span data-stu-id="8dd36-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="8dd36-188">**\_host de serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="8dd36-189">Um tipo opaco usado para fazer referência a um host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="8dd36-190">Estrutura</span><span class="sxs-lookup"><span data-stu-id="8dd36-190">Structure</span></span>                                                                              | <span data-ttu-id="8dd36-191">Description</span><span class="sxs-lookup"><span data-stu-id="8dd36-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="8dd36-192">**ponto de extremidade de \_ serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="8dd36-193">Representa um ponto de extremidade individual em um host de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="8dd36-194">**\_propriedade de \_ ponto de extremidade de serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="8dd36-195">Especifica uma configuração específica do serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="8dd36-196">**\_Propriedade do serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="8dd36-197">Especifica uma configuração específica do serviço.</span><span class="sxs-lookup"><span data-stu-id="8dd36-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="8dd36-198">**\_retorno de \_ chamada de aceitação de Propriedade do serviço WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="8dd36-199">Especifica o retorno de chamada que é chamado quando um canal é aceito com êxito.</span><span class="sxs-lookup"><span data-stu-id="8dd36-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="8dd36-200">**\_retorno de \_ chamada de fechamento da propriedade de serviço WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8dd36-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="8dd36-201">Especifica o retorno de chamada que é chamado quando um canal está prestes a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="8dd36-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




