---
title: Importação de metadados
description: O WWSAPI inclui elementos de API que podem ser usados para processar WSDL e a política de um ponto de extremidade com o objetivo de extrair informações que podem ser usadas para se comunicar com o ponto de extremidade.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Serviços Web de importação de metadados para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103643022"
---
# <a name="metadata-import"></a><span data-ttu-id="40278-106">Importação de metadados</span><span class="sxs-lookup"><span data-stu-id="40278-106">Metadata Import</span></span>

<span data-ttu-id="40278-107">O WWSAPI inclui elementos de API que podem ser usados para processar WSDL e a política de um ponto de extremidade com o objetivo de extrair informações que podem ser usadas para se comunicar com o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="40278-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="40278-108">Essas APIs normalmente são usadas quando o protocolo de comunicação com suporte do ponto de extremidade ainda não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="40278-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="40278-109">Use a seguinte sequência para processar metadados:</span><span class="sxs-lookup"><span data-stu-id="40278-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="40278-110">para obter informações sobre como as declarações WSDL e WS-Policy correspondem à API, consulte o tópico [mapeamento de metadados](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="40278-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="40278-111">Segurança</span><span class="sxs-lookup"><span data-stu-id="40278-111">Security</span></span>

<span data-ttu-id="40278-112">Os metadados baixados são tão bons quanto o endereço usado para baixá-lo.</span><span class="sxs-lookup"><span data-stu-id="40278-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="40278-113">Um aplicativo deve garantir que o é confiável para o endereço.</span><span class="sxs-lookup"><span data-stu-id="40278-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="40278-114">Além disso, um aplicativo deve garantir que ele use um protocolo de segurança para baixar os documentos de metadados que não permitem a violação dos metadados.</span><span class="sxs-lookup"><span data-stu-id="40278-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="40278-115">Um aplicativo deve inspecionar os endereços dos serviços expostos pelos metadados.</span><span class="sxs-lookup"><span data-stu-id="40278-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="40278-116">Por padrão, o tempo de execução garante que o nome do host do serviço corresponda ao da URL original usada para baixar os metadados, mas o aplicativo pode querer executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="40278-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="40278-117">Um aplicativo pode desabilitar a verificação de nome de host, substituindo a propriedade de [**nomes de host de verificação de \_ propriedade de metadados \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) .</span><span class="sxs-lookup"><span data-stu-id="40278-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="40278-118">Se a verificação de nome de host feita por padrão for desabilitada, o aplicativo precisará se proteger contra os documentos de metadados que contêm o endereço de um serviço de uma parte diferente da qual ele não confia de alguma outra maneira.</span><span class="sxs-lookup"><span data-stu-id="40278-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="40278-119">Por padrão, a quantidade máxima de memória usada pelo tempo de execução de metadados para desserializar e processar os metadados é de 256 k, e o número máximo de documentos que podem ser adicionados é 32.</span><span class="sxs-lookup"><span data-stu-id="40278-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="40278-120">Esses valores padrão podem ser substituídos pelas propriedades de documentos [**\_ \_ \_ \_ \_ tamanho solicitado de heap de propriedade de metadados WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) e **\_ \_ propriedade \_ máxima \_ de metadados do WS** .</span><span class="sxs-lookup"><span data-stu-id="40278-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="40278-121">Esses limites foram projetados para limitar a quantidade de downloads e limitar a quantidade de memória alocada para acumular os metadados.</span><span class="sxs-lookup"><span data-stu-id="40278-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="40278-122">Aumentar esses valores pode levar a uso excessivo de memória, uso de CPU ou consumo de largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="40278-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="40278-123">Observe que, devido à expansão de cadeias de caracteres de dicionário no formato binário, uma mensagem pequena pode levar a uma forma desserializada muito maior, portanto, depender de mensagens pequenas para limitar a alocação de memória de metadados não é suficiente ao usar o formato binário.</span><span class="sxs-lookup"><span data-stu-id="40278-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="40278-124">Por padrão, o número máximo de alternativas de política é 32, embora possa ser substituído pela propriedade [**de \_ \_ \_ \_ alternativas máximas da propriedade de política do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) .</span><span class="sxs-lookup"><span data-stu-id="40278-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="40278-125">Se um aplicativo executar um loop por cada alternativa procurando uma correspondência, talvez seja necessário pesquisar todas as alternativas antes de localizar uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="40278-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="40278-126">Aumentar o número máximo de alternativas pode levar à utilização excessiva da CPU.</span><span class="sxs-lookup"><span data-stu-id="40278-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="40278-127">As seguintes enumerações fazem parte da importação de metadados:</span><span class="sxs-lookup"><span data-stu-id="40278-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="40278-128">**\_ID da \_ propriedade de metadados do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="40278-129">**\_estado de metadados do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="40278-130">**\_tipo de \_ extensão da política WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="40278-131">**\_ID da \_ propriedade da política do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="40278-132">**\_estado da política WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="40278-133">**\_tipo de \_ restrição de associação de segurança WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="40278-134">As funções a seguir fazem parte da importação de metadados:</span><span class="sxs-lookup"><span data-stu-id="40278-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="40278-135">**WsCreateMetadata**</span><span class="sxs-lookup"><span data-stu-id="40278-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="40278-136">**WsFreeMetadata**</span><span class="sxs-lookup"><span data-stu-id="40278-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="40278-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="40278-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="40278-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="40278-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="40278-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="40278-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="40278-140">**WsGetPolicyAlternativeCount**</span><span class="sxs-lookup"><span data-stu-id="40278-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="40278-141">**WsGetPolicyProperty**</span><span class="sxs-lookup"><span data-stu-id="40278-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="40278-142">**WsMatchPolicyAlternative**</span><span class="sxs-lookup"><span data-stu-id="40278-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="40278-143">**WsReadMetadata**</span><span class="sxs-lookup"><span data-stu-id="40278-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="40278-144">**WsResetMetadata**</span><span class="sxs-lookup"><span data-stu-id="40278-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="40278-145">Os seguintes identificadores fazem parte da importação de metadados:</span><span class="sxs-lookup"><span data-stu-id="40278-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="40278-146">metadados do WS \_</span><span class="sxs-lookup"><span data-stu-id="40278-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="40278-147">\_política WS</span><span class="sxs-lookup"><span data-stu-id="40278-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="40278-148">As seguintes estruturas fazem parte da importação de metadados:</span><span class="sxs-lookup"><span data-stu-id="40278-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="40278-149">**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="40278-150">**\_restrição de \_ Propriedade do canal WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="40278-151">**extensão de política de ponto de \_ extremidade WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="40278-152">**\_restrição de \_ \_ Associação de segurança de autenticação de cabeçalho \_ http \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="40278-153">**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="40278-154">**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="40278-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="40278-155">**ponto de extremidade de \_ metadados do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="40278-156">**pontos de extremidade de \_ metadados do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="40278-157">**\_propriedade de metadados WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="40278-158">**\_restrições de política do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="40278-159">**\_extensão de política WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="40278-160">**\_Propriedades da política do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="40278-161">**\_propriedade de política WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="40278-162">**\_restrição de \_ propriedade de token de segurança de solicitação WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="40278-163">**\_restrição de \_ Associação de segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="40278-164">**\_restrição de \_ propriedade de associação de segurança WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="40278-165">**\_restrições de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="40278-166">**\_restrição de \_ \_ Associação de segurança de mensagem de contexto \_ de \_ segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="40278-167">**\_restrição de \_ propriedade de segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="40278-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="40278-168">**\_restrição de \_ Associação de segurança de transporte WS SSL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="40278-169">**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="40278-170">**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40278-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




