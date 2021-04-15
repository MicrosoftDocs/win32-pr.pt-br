---
title: Metadados de serviço
description: O host do serviço WWSAPI dá suporte a WS-MetadataExchange para seus pontos de extremidade.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Metadados de serviço nativos-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454466"
---
# <a name="service-metadata"></a><span data-ttu-id="98781-106">Metadados de serviço</span><span class="sxs-lookup"><span data-stu-id="98781-106">Service Metadata</span></span>

<span data-ttu-id="98781-107">O host do serviço WWSAPI dá suporte a WS-MetadataExchange para seus pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="98781-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="98781-108">Você habilita essa troca de metadados no host de serviço com as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="98781-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="98781-109">Especifique documentos de metadados na propriedade de [**\_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) no [ \_ \_ host do serviço WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="98781-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="98781-110">Especifique o nome do serviço na propriedade de [**\_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) no [ \_ \_ host do serviço WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="98781-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="98781-111">Especifique a porta para pontos de extremidade individuais usando a propriedade [**de \_ \_ metadados de \_ propriedade \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) de ponto de extremidade de serviço WS no [**ponto de \_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="98781-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="98781-112">Habilite uma ou mais estruturas de [**\_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) para atender às solicitações de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="98781-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="98781-113">Opcionalmente, especifique **o \_ \_ sufixo de \_ \_ \_ \_ URL \_ da propriedade de ponto de extremidade de serviço WS** na enumeração de [**\_ \_ \_ \_ ID de Propriedade do ponto de extremidade**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) do serviço WS para atender às solicitações de Ws-MetadataExchange em um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="98781-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="98781-114">Especificando os documentos de metadados/nome do serviço no host de serviço</span><span class="sxs-lookup"><span data-stu-id="98781-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="98781-115">A primeira etapa é especificar os documentos de metadados no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="98781-116">Faça isso reunindo os documentos individuais como uma matriz de \_ \_ cadeias de caracteres XML \* do WS.</span><span class="sxs-lookup"><span data-stu-id="98781-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="98781-117">Essas cadeias de caracteres podem ser o esquema XML, o WSDL ou o documento WS-Policy.</span><span class="sxs-lookup"><span data-stu-id="98781-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="98781-118">Isso é especificado por meio da propriedade de [**\_ metadados de \_ propriedade \_ do serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="98781-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="98781-119">Opcionalmente, um aplicativo também pode especificar o nome do serviço e o namespace como parte [**dos \_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span><span class="sxs-lookup"><span data-stu-id="98781-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="98781-120">Se o documento de metadados não especificar o elemento de serviço para o nome de serviço fornecido, o modelo de serviço irá gerar um elemento de serviço com as portas WSDL correspondentes para o serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="98781-121">Observe que nenhuma verificação dos documentos de metadados individuais será executada nos documentos.</span><span class="sxs-lookup"><span data-stu-id="98781-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="98781-122">É responsabilidade do aplicativo validar o conteúdo dos documentos e garantir que todos os caminhos de importações sejam relativamente especificados.</span><span class="sxs-lookup"><span data-stu-id="98781-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="98781-123">O namespace especificado é usado para localizar o documento no qual o elemento de serviço será adicionado pelo host de serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="98781-124">Adição do elemento de serviço ao documento WSDL</span><span class="sxs-lookup"><span data-stu-id="98781-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="98781-125">O host de serviço fornece recursos para que o aplicativo adicione um elemento de serviço em seu nome, se um já não estiver especificado.</span><span class="sxs-lookup"><span data-stu-id="98781-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="98781-126">Para habilitar esse comportamento, um aplicativo deve especificar os campos serivceName e serviceNs na estrutura [**de \_ \_ metadados do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) .</span><span class="sxs-lookup"><span data-stu-id="98781-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="98781-127">Se ServiceName e serviceNs forem **nulos** , nenhum elemento de serviço será adicionado ao documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="98781-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="98781-128">Ambos são usados para identificar o documento no qual o ServiceElement será adicionado.</span><span class="sxs-lookup"><span data-stu-id="98781-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="98781-129">Se a propriedade de [**\_ metadados de \_ propriedade \_ do serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) não for especificada, nenhum metadado transhanging ocorrerá no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="98781-130">Especificando a porta no ponto de \_ extremidade do serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="98781-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="98781-131">Para que [**um \_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) esteja disponível como uma porta dentro do elemento de serviço no documento WSDL, o aplicativo deve especificar a propriedade de [**\_ \_ \_ \_ metadados de propriedade de ponto de extremidade de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .</span><span class="sxs-lookup"><span data-stu-id="98781-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="98781-132">Supõe-se que a referência ao nome de associação e ao namespace exista nos documentos especificados no host de serviço como parte dos \_ metadados de Propriedade do serviço WS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="98781-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="98781-133">O tempo de execução não verifica isso em nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98781-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="98781-134">Habilitar serviço de WS-MetadataExchange no \_ ponto de extremidade de serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="98781-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="98781-135">Para atender às solicitações de WS-MetadataExchange, o host de serviço deve ter pelo menos um ponto de extremidade habilitado para atender a solicitações de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="98781-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="98781-136">Isso é feito definindo a versão apropriada para WS-MetadataExchange no ponto de [**\_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="98781-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="98781-137">Habilitar serviço GET HTTP no ponto de extremidade de \_ serviço WS \_</span><span class="sxs-lookup"><span data-stu-id="98781-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="98781-138">Para solicitações GET de CreateHttp, o host de serviço deve ter pelo menos um ponto de extremidade habilitado para atender a solicitações de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="98781-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="98781-139">Isso é feito definindo a versão apropriada para WS-MetadataExchange no ponto de [**\_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="98781-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="98781-140">Especificando o sufixo de URL para solicitações de Ws-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="98781-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="98781-141">Opcionalmente, um aplicativo pode habilitar apenas a aceitação de solicitações para WS-MetadataExchange em um caminho específico.</span><span class="sxs-lookup"><span data-stu-id="98781-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="98781-142">Isso é feito especificando um sufixo para o ponto de extremidade de serviço WS especificado \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="98781-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="98781-143">Esse sufixo é concatenado no estado em que se encontra para a URL real para o \_ ponto de extremidade do serviço WS \_ .</span><span class="sxs-lookup"><span data-stu-id="98781-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="98781-144">A cadeia de caracteres concatenada é usada como a URL correspondente ao cabeçalho ' to ' recebido.</span><span class="sxs-lookup"><span data-stu-id="98781-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="98781-145">Os elementos da API a seguir estão relacionados ao serviço metadados.</span><span class="sxs-lookup"><span data-stu-id="98781-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="98781-146">Enumeração</span><span class="sxs-lookup"><span data-stu-id="98781-146">Enumeration</span></span>                                                       | <span data-ttu-id="98781-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="98781-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="98781-148">**\_tipo de \_ troca de metadados WS \_**</span><span class="sxs-lookup"><span data-stu-id="98781-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="98781-149">Habilita ou desabilita a manutenção de WS-MetadataExchange e HTTP GET no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="98781-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="98781-150">Estrutura</span><span class="sxs-lookup"><span data-stu-id="98781-150">Structure</span></span>                                                               | <span data-ttu-id="98781-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="98781-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="98781-152">**\_metadados de \_ ponto de extremidade de serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="98781-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="98781-153">Representa o elemento Port para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="98781-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="98781-154">**\_metadados do serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="98781-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="98781-155">Especifica a matriz de documentos de metadados de serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="98781-156">**\_documento de \_ metadados do serviço WS \_**</span><span class="sxs-lookup"><span data-stu-id="98781-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="98781-157">Especifica os documentos individuais que compõem os metadados do serviço.</span><span class="sxs-lookup"><span data-stu-id="98781-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




