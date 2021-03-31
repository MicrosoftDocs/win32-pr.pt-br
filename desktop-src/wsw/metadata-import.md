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
# <a name="metadata-import"></a>Importação de metadados

O WWSAPI inclui elementos de API que podem ser usados para processar WSDL e a política de um ponto de extremidade com o objetivo de extrair informações que podem ser usadas para se comunicar com o ponto de extremidade. Essas APIs normalmente são usadas quando o protocolo de comunicação com suporte do ponto de extremidade ainda não é conhecido.


Use a seguinte sequência para processar metadados:

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

para obter informações sobre como as declarações WSDL e WS-Policy correspondem à API, consulte o tópico [mapeamento de metadados](metadata-mapping.md) .

## <a name="security"></a>Segurança

Os metadados baixados são tão bons quanto o endereço usado para baixá-lo. Um aplicativo deve garantir que o é confiável para o endereço. Além disso, um aplicativo deve garantir que ele use um protocolo de segurança para baixar os documentos de metadados que não permitem a violação dos metadados.

Um aplicativo deve inspecionar os endereços dos serviços expostos pelos metadados. Por padrão, o tempo de execução garante que o nome do host do serviço corresponda ao da URL original usada para baixar os metadados, mas o aplicativo pode querer executar verificações adicionais. Um aplicativo pode desabilitar a verificação de nome de host, substituindo a propriedade de [**nomes de host de verificação de \_ propriedade de metadados \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) . Se a verificação de nome de host feita por padrão for desabilitada, o aplicativo precisará se proteger contra os documentos de metadados que contêm o endereço de um serviço de uma parte diferente da qual ele não confia de alguma outra maneira.

Por padrão, a quantidade máxima de memória usada pelo tempo de execução de metadados para desserializar e processar os metadados é de 256 k, e o número máximo de documentos que podem ser adicionados é 32. Esses valores padrão podem ser substituídos pelas propriedades de documentos [**\_ \_ \_ \_ \_ tamanho solicitado de heap de propriedade de metadados WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) e **\_ \_ propriedade \_ máxima \_ de metadados do WS** . Esses limites foram projetados para limitar a quantidade de downloads e limitar a quantidade de memória alocada para acumular os metadados. Aumentar esses valores pode levar a uso excessivo de memória, uso de CPU ou consumo de largura de banda de rede. Observe que, devido à expansão de cadeias de caracteres de dicionário no formato binário, uma mensagem pequena pode levar a uma forma desserializada muito maior, portanto, depender de mensagens pequenas para limitar a alocação de memória de metadados não é suficiente ao usar o formato binário.

Por padrão, o número máximo de alternativas de política é 32, embora possa ser substituído pela propriedade [**de \_ \_ \_ \_ alternativas máximas da propriedade de política do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) . Se um aplicativo executar um loop por cada alternativa procurando uma correspondência, talvez seja necessário pesquisar todas as alternativas antes de localizar uma correspondência. Aumentar o número máximo de alternativas pode levar à utilização excessiva da CPU.

As seguintes enumerações fazem parte da importação de metadados:

-   [**\_ID da \_ propriedade de metadados do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**\_estado de metadados do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**\_tipo de \_ extensão da política WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**\_ID da \_ propriedade da política do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**\_estado da política WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**\_tipo de \_ restrição de associação de segurança WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

As funções a seguir fazem parte da importação de metadados:

-   [**WsCreateMetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**WsFreeMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**WsGetPolicyAlternativeCount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**WsGetPolicyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**WsMatchPolicyAlternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**WsReadMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**WsResetMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

Os seguintes identificadores fazem parte da importação de metadados:

-   [metadados do WS \_](ws-metadata.md)
-   [\_política WS](ws-policy.md)

As seguintes estruturas fazem parte da importação de metadados:

-   [**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restrição de \_ Propriedade do canal WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**extensão de política de ponto de \_ extremidade WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**\_restrição de \_ \_ Associação de segurança de autenticação de cabeçalho \_ http \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**ponto de extremidade de \_ metadados do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**pontos de extremidade de \_ metadados do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**\_propriedade de metadados WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**\_restrições de política do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**\_extensão de política WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**\_Propriedades da política do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**\_propriedade de política WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**\_restrição de \_ propriedade de token de segurança de solicitação WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**\_restrição de \_ Associação de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**\_restrição de \_ propriedade de associação de segurança WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**\_restrições de segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem de contexto \_ de \_ segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**\_restrição de \_ propriedade de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**\_restrição de \_ Associação de segurança de transporte WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




