---
title: Suporte de política
description: Wsutil processa a política especificada nos metadados de entrada e gera rotinas auxiliares para o suporte ao modelo de serviço.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Serviços Web de suporte de política para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838636"
---
# <a name="policy-support"></a>Suporte de política

Wsutil processa a política especificada nos metadados de entrada e gera rotinas auxiliares para o suporte ao modelo de serviço.

## <a name="how-to-use-policy-support-in-wsutil"></a>Como usar o suporte a políticas no Wsutil

Os desenvolvedores devem seguir as seguintes etapas para usar o suporte de política no compilador Wsutil:

-   Colete todos os arquivos de metadados de entrada necessários para o serviço Web de destino.
-   Compile todos os arquivos WSDL/XSD/Policy coletados usando wsutil.exe. O Wsutil gera um conjunto de arquivos stub e arquivo de cabeçalho para cada arquivos WSDL e XSD de entrada.
-   Inspecione o arquivo de cabeçalho gerado, todos os nomes de rotina do auxiliar de política estão listados na seção comentário no início do arquivo de cabeçalho.
-   Use \_ a rotina auxiliar CreateServiceProxy de BindingName para criar o proxy de serviço.
-   Use \_ a rotina auxiliar CreateServiceEndpoint de vinculação para criar um ponto de extremidade de serviço.
-   Preencha \_ a estrutura de modelo de associação do WS bindingTemplateType \_ \_ especificada na assinatura do método. Os desenvolvedores podem fornecer propriedades de canal adicionais e/ou propriedades de segurança, conforme necessário.
-   Chame as rotinas auxiliares, em proxy de serviço de retorno bem-sucedido ou ponto de extremidade de serviço é criado.

As seções a seguir descrevem os tópicos relacionados em detalhes.

## <a name="handle-policy-input"></a>Processar entrada de política

Veja a seguir as [Opções de compilador](web-service-compiler-tool.md) relacionadas ao processamento de política.

Por padrão, o Wsutil sempre gerará modelos de política, a menos que seja chamado com a opção "/nopolicy". A política pode ser incorporada como parte de um arquivo WSDL ou pode ser criada separadamente como um arquivo de metadados de política que o Wsutil usa como entrada. A opção de compilador "/WSP:" é usada para indicar que os metadados de entrada especificados são um arquivo de política. O Wsutil gera possíveis auxiliares relacionados à política com a seguinte compilação:

**Wsutil/WSDL:/WSDL confiável. WSDL: TRUSTED1. WSDL**

**wstuil/WSDL: Input. WSDL/WSP: Policy. wsp**

Nenhum auxiliar de política é gerado quando a opção "/nopolicy" é usada como no exemplo a seguir.

**Wsutil/nopolicy/WSDL: Trusted. WSDL/WSDL: TRUSTED1. WSDL**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Código relacionado à política gerado pelo compilador Wsutil

A página [mapeamento de metadados](metadata-mapping.md) detalha o mapeamento entre os constructos de metadados com diferentes tipos de associação.

Três categorias de configurações de política podem ser especificadas nas configurações de política:

-   Propriedades do canal. Atualmente, apenas as seguintes propriedades de canal têm suporte: [**codificação de propriedade de canal de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **\_ \_ \_ \_ versão de endereçamento** de Propriedade do WS Channel e **versão de envelope de Propriedade do WS \_ Channel \_ \_ \_**.
-   Propriedades de segurança. Atualmente, há suporte apenas para as seguintes propriedades de segurança: [**\_ uso de carimbo de \_ \_ Data/ \_ hora de propriedade de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **\_ \_ \_ \_ \_ layout de cabeçalho de segurança** de propriedade de segurança WS, **\_ \_ \_ \_ \_ nível de proteção de transporte** de propriedade de segurança do WS e **\_ \_ \_ \_ \_ versão do cabeçalho**
-   Associação de segurança. Atualmente, somente as seguintes associações de segurança têm suporte [**: \_ \_ Associação de \_ \_ segurança \_ de autenticação de cabeçalho WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding), associação de segurança de [**\_ transporte WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), associação de [**segurança de \_ transporte WS TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding), [**\_ Associação de segurança de \_ mensagem WS \_ \_ username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), [**Associação de segurança de \_ mensagem WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)e Associação de [**segurança de mensagem de \_ contexto de segurança \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).

Tipo de modelo de associação

Há números limitados de associações com suporte no Wsutil. Todas essas combinações com suporte dessas associações estão listadas na definição do [**tipo de modelo de associação do WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) . Por exemplo, para a seguinte associação em WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Wsutil gera o tipo de modelo de associação de [**\_ tipo de \_ \_ modelo \_ de associação http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) para esta associação.

Descrições de política

Com a configuração de política de entrada, o Wsutil gera um conjunto de descrições de política que descrevem a política de entrada, incluindo o tipo de modelo, bem como os valores especificados na política. Por exemplo, para entrada

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

Wsutil gera a descrição da propriedade de canal como:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Todas as configurações de política (Propriedades de canal, propriedades de segurança e propriedades de associação de segurança) em uma associação são agregadas em uma estrutura de descrição de política do WS \_ bindingTemplateType \_ \_ . [**WS \_ \_ \_ Tipo de modelo de associação**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) especifica as diferentes combinações de política de associação que o Wsutil dá suporte.

Estrutura de modelo a ser preenchida pelo aplicativo

A descrição da política contém todas as informações de política especificadas nos metadados de entrada para uma determinada associação, mas há informações que não podem ser representadas na política ainda exigem a entrada do usuário ao usar essas políticas para criar proxy de serviço e/ou ponto de extremidade de serviço. Por exemplo, o aplicativo deve fornecer credenciais para autenticação de cabeçalho HTTP.

O aplicativo precisa preencher a estrutura do modelo, denominada \_ \_ modelo de associação WS bindingTemplateType \_ para cada tipo de modelo de associação diferente, definido em WebServices. h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

A lista de modelos de associação de segurança é opcional depende da Associação de segurança correspondente. Por exemplo, o campo [**modelo de associação de segurança de transporte do WS \_ SSL \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) é apresentado no [**\_ \_ \_ \_ modelo de associação SSL WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) para o aplicativo fornecer informações de associação de segurança relacionadas a SSL, incluindo as informações de credenciais.

O aplicativo precisa preencher todos os campos nesta estrutura antes de chamar as APIs de modelo do WebServices. Propriedades de segurança adicionais, bem como propriedades de associação de segurança que não podem ser representes na política, precisam ser preenchidas e as APIs de WebServices mesclam o dois conjuntos de propriedades no tempo de execução. Os campos podem ser zerados se não forem aplicáveis. Por exemplo, securityProperties pode ser zerado se nenhuma propriedade de segurança adicional for necessária.

Rotinas auxiliares e declaração de descrição de política em arquivos de cabeçalho

o Wsutil cria uma rotina auxiliar para facilitar o suporte na camada do modelo de serviço, de modo que o aplicativo pode criar proxy de serviço e ponto de extremidade de serviço mais fácil. A descrição da política também é exposta de modo que o aplicativo possa usá-las diretamente. Uma rotina de ajuda do CreateSerivceProxy é semelhante a:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Os desenvolvedores são incentivados a usar essas rotinas auxiliares, embora também possam usar diretamente a rotina de tempo de execução subjacente fornecida pelo webservices.dll. Os desenvolvedores não são incentivados a usar as descrições de política diretamente ao programar usando a camada do [modelo de serviço](service-model-layer-overview.md) .

Referências de descrição de política também são geradas no cabeçalho para usuário avançado. Se os desenvolvedores não usam funcionalidades de modelo de serviço, eles podem usar as descrições de política diretamente.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Protótipos de definição em arquivos de stub

Um campo de estrutura de descrição de política única por associação e suas descrições auxiliares referenciadas internamente são criadas na estrutura do protótipo local. As descrições de política são geradas no arquivo onde [**a \_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) é gerada. Geralmente, os desenvolvedores não precisam inspecionar o arquivo stub durante o desenvolvimento, embora o arquivo stub contenha todos os detalhes sobre as especificações da política.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Implementação de rotinas auxiliares nos arquivos stub

O Wsutil gera rotinas auxiliares para simplificar as chamadas de aplicativo para [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) e criar base de [**ponto de \_ \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) nas informações fornecidas nas configurações de política.

Depende das restrições de associação especificadas para a porta determinada, o primeiro argumento é diferente de acordo com a estrutura do modelo. O exemplo a seguir pressupõe o transporte HTTP, a assinatura para a criação do proxy de serviço é semelhante a um parâmetro de tipo de canal adicional.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Configurações de política com suporte

A tabela a seguir lista todos os tipos de modelo de associação com suporte, as associações de segurança correspondentes necessárias no tipo, a estrutura do modelo a ser preenchida pelo aplicativo para o tipo e o tipo de descrição correspondente. O aplicativo precisa preencher a estrutura do modelo, enquanto o desenvolvedor do aplicativo deve entender quais são as associações de segurança necessárias na política determinada.



| [**\_tipo de \_ modelo de associação WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Combinações de associação de segurança                                                                                                                                                                                                                                                                                                               | estrutura de modelo a ser preenchida pelo aplicativo                                                                                            | Descrição da política                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ modelo de associação http \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_modelo de \_ Associação \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**\_Descrição da \_ política \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_tipo de \_ \_ modelo de associação SSL WS http \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_Associação de \_ segurança de transporte WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_modelo de \_ \_ Associação SSL WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**\_Descrição da \_ \_ política SSL \_ do WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_tipo de \_ \_ modelo de associação de autenticação de cabeçalho \_ http \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**\_Associação de \_ \_ segurança de autenticação de cabeçalho http \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_modelo de \_ \_ Associação de autenticação de cabeçalho http \_ do \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**\_Descrição da \_ \_ política de autenticação de cabeçalho http \_ do \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_tipo de \_ \_ modelo de \_ Associação de autenticação de cabeçalho SSL \_ \_ \_ do WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**WS \_ Associação \_ de \_ segurança \_ de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [ **\_ \_ \_ \_ \_ Associação de autenticação de cabeçalho WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_modelo de \_ \_ Associação de autenticação de cabeçalho SSL \_ \_ do WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**\_Descrição da \_ \_ política de autenticação de cabeçalho SSL \_ \_ do WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_tipo de \_ \_ modelo de associação de nome de usuário SSL \_ \_ WS http \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ Ligação \_ de \_ segurança \_ de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e [ **\_ Associação de segurança de \_ mensagem \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_modelo de \_ \_ Associação de nome de usuário SSL \_ WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**DESCRIÇÃO DA POLÍTICA DE \_ \_ NOME DE USUÁRIO SSL \_ \_ HTTP DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**WS \_ HTTP \_ SSL TIPO DE MODELO DE ASSOCIAÇÃO \_ KERBEROS \_ \_ APREQ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) E ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [ **\_ DO WS KERBEROS \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**MODELO DE \_ ASSOCIAÇÃO \_ \_ KERBEROS \_ APREQ DO WS HTTP \_ SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**TIPO DE MODELO \_ DE ASSOCIAÇÃO TCP \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**MODELO DE \_ ASSOCIAÇÃO TCP \_ DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**DESCRIÇÃO \_ DA POLÍTICA TCP \_ DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**TIPO DE \_ MODELO DE \_ ASSOCIAÇÃO SSPI TCP \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**ASSOCIAÇÃO DE SEGURANÇA \_ DE TRANSPORTE \_ SSPI TCP \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**MODELO DE \_ ASSOCIAÇÃO \_ SSPI TCP \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**DESCRIÇÃO \_ DA POLÍTICA \_ SSPI TCP \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**TIPO DE MODELO DE ASSOCIAÇÃO DE NOME DE USUÁRIO \_ \_ TCP SSPI \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA \_ DE TRANSPORTE TCP SSPI \_ \_ \_ E**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO DO [ **\_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**MODELO DE ASSOCIAÇÃO DE NOME DE \_ USUÁRIO \_ SSPI TCP \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**DESCRIÇÃO DA POLÍTICA DE NOME DE \_ USUÁRIO \_ SSPI TCP \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**TIPO DE MODELO DE ASSOCIAÇÃO \_ \_ \_ KERBEROS \_ APREQ \_ \_ DO WS TCP SSPI \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**WS \_ ASSOCIAÇÃO DE \_ SEGURANÇA DE TRANSPORTE DO SSPI \_ \_ \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) E ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [ **\_ \_ KERBEROS APREQ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**MODELO DE \_ ASSOCIAÇÃO \_ \_ KERBEROS \_ APREQ \_ \_ DO WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**TIPO DE MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA DO NOME DE USUÁRIO \_ \_ SSL \_ \_ \_ \_ \_ \_ HTTP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE SSL e \_ \_ \_ ASSOCIAÇÃO**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do WS COM ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO do WS no canal de inicialização [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                         | [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA DE NOME \_ \_ DE USUÁRIO SSL \_ \_ \_ \_ HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**DESCRIÇÃO DA POLÍTICA DE CONTEXTO DE SEGURANÇA DO NOME \_ \_ DE USUÁRIO SSL \_ \_ \_ \_ HTTP \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**TIPO DE MODELO DE ASSOCIAÇÃO DE CONTEXTO DE \_ SEGURANÇA WS HTTP \_ SSL \_ KERBEROS \_ APREQ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA DE \_ TRANSPORTE \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) e ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do [**WS com A ASSOCIAÇÃO DE SEGURANÇA \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) DE MENSAGEM [**\_ APREQ DO WS KERBEROS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) no canal de inicialização            | [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA \_ \_ \_ KERBEROS \_ APREQ DO WS HTTP \_ \_ \_ SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**TIPO DE MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA DO NOME DE USUÁRIO \_ \_ SSPI DO \_ \_ \_ \_ \_ WS TCP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA \_ DE TRANSPORTE TCP SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do [**WS com ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) USUÁRIO do [**WS \_ no \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) canal de inicialização              | [**MODELO DE ASSOCIAÇÃO DE \_ CONTEXTO DE SEGURANÇA DO NOME DE USUÁRIO \_ SSPI DO \_ \_ \_ \_ \_ WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**TIPO DE MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA \_ \_ \_ KERBEROS \_ APREQ \_ \_ \_ \_ DO WS \_ TCP SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**WS \_ ASSOCIAÇÃO DE SEGURANÇA \_ DE TRANSPORTE TCP SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) e ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE [**SEGURANÇA WS com A ASSOCIAÇÃO DE SEGURANÇA \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) DE MENSAGEM [**\_ APREQ WS KERBEROS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) no canal de inicialização | [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA \_ \_ \_ KERBEROS \_ APREQ \_ \_ \_ DO WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Por exemplo, [**WS \_ HTTP \_ SSL \_ BINDING TEMPLATE \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) indica que a política de entrada para a associação especifica o transporte HTTP e a ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ SSL \_ \_ \_ do WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). O aplicativo precisa preencher a estrutura MODELO DE ASSOCIAÇÃO [**\_ \_ SSL \_ \_ HTTP do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) antes de chamar as rotinas auxiliares, e a descrição da política correspondente é [**WS HTTP \_ \_ SSL \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). Mais especificamente, a seção de associação no WSDL contém os seguintes segmentos:

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Suporte ao contexto de segurança

No [Contexto de Segurança](security-context.md), o canal de inicialização é criado para estabelecer a conversa segura no canal de serviço. O Wsutil dá suporte apenas ao cenário em que o canal de inicialização é o mesmo que o canal de serviço, com as mesmas propriedades de canal e propriedades de segurança. A segurança de transporte é necessária para a associação de mensagens de contexto de segurança; O wsutil dá suporte a canais de inicialização com outras vinculações de segurança de mensagem, mas só dá suporte ao contexto de segurança como a única associação de segurança de mensagem no canal de serviço, sem combinação com outras vinculações de segurança de mensagem. Os desenvolvedores podem dar suporte a essas combinações fora do suporte ao modelo de política.

A enumeração a seguir faz parte do suporte à política:

-   [**TIPO DE MODELO \_ DE ASSOCIAÇÃO \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

As seguintes funções fazem parte do suporte à política:

-   [**WsCreateServiceEndpointFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**WsCreateServiceProxyFromTemplate**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

As seguintes estruturas fazem parte do suporte à política:

-   [**MODELO DE \_ ASSOCIAÇÃO HTTP \_ DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**MODELO DE \_ ASSOCIAÇÃO \_ DE \_ AUTENTICAÇÃO DE CABEÇALHO HTTP \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**DESCRIÇÃO \_ DA POLÍTICA DE \_ \_ AUTENTICAÇÃO DE \_ \_ CABEÇALHO HTTP DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA \_ \_ DE \_ AUTENTICAÇÃO \_ \_ \_ \_ DE CABEÇALHO HTTP DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DE AUTENTICAÇÃO DE CABEÇALHO \_ HTTP \_ \_ \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**DESCRIÇÃO \_ DA POLÍTICA HTTP \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**MODELO DE \_ ASSOCIAÇÃO \_ SSL HTTP DO \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**MODELO DE ASSOCIAÇÃO DE AUTENTICAÇÃO DE CABEÇALHO \_ \_ SSL HTTP \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE AUTENTICAÇÃO DO CABEÇALHO \_ \_ HTTP SSL \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**MODELO DE \_ ASSOCIAÇÃO \_ \_ KERBEROS \_ APREQ DO WS HTTP \_ SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA \_ \_ \_ KERBEROS \_ APREQ DO WS HTTP \_ \_ \_ SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**WS \_ HTTP \_ SSL \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**DESCRIÇÃO \_ DA \_ POLÍTICA SSL HTTP DO \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE \_ NOME \_ DE USUÁRIO SSL HTTP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE \_ \_ NOME DE USUÁRIO SSL \_ \_ HTTP DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA DE NOME \_ \_ DE USUÁRIO SSL \_ \_ \_ \_ HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE CONTEXTO DE SEGURANÇA DO NOME \_ \_ DE USUÁRIO SSL \_ \_ \_ \_ HTTP \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM \_ \_ KERBEROS APREQ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA DA MENSAGEM DE CONTEXTO \_ \_ DE \_ \_ \_ \_ SEGURANÇA DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DA MENSAGEM \_ \_ DE CONTEXTO DE \_ \_ \_ SEGURANÇA DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA DO CONTEXTO DE SEGURANÇA \_ \_ \_ \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE \_ SEGURANÇA DE CONTEXTO DE \_ \_ \_ SEGURANÇA DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA DE \_ TRANSPORTE SSL \_ \_ \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE \_ SSL \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE DO \_ SSPI \_ \_ \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**MODELO DE \_ ASSOCIAÇÃO TCP \_ DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**DESCRIÇÃO \_ DA POLÍTICA TCP \_ DO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**MODELO DE \_ ASSOCIAÇÃO \_ SSPI TCP \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**MODELO DE \_ ASSOCIAÇÃO \_ \_ KERBEROS \_ APREQ \_ \_ DO WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE CONTEXTO DE SEGURANÇA \_ \_ \_ KERBEROS \_ APREQ \_ \_ \_ DO WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ KERBEROS \_ APREQ \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**DESCRIÇÃO \_ DA POLÍTICA \_ SSPI TCP \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE \_ \_ SSPI TCP \_ \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**MODELO DE ASSOCIAÇÃO DE NOME DE \_ USUÁRIO \_ SSPI TCP \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**DESCRIÇÃO DA POLÍTICA DE NOME DE \_ USUÁRIO \_ SSPI TCP \_ \_ DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE \_ CONTEXTO DE SEGURANÇA DO NOME DE USUÁRIO \_ SSPI DO \_ \_ \_ \_ \_ WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**WS \_ TCP \_ SSPI \_ USERNAME \_ SECURITY \_ CONTEXT \_ POLICY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**DESCRIÇÃO DA POLÍTICA DE ASSOCIAÇÃO DE SEGURANÇA DA MENSAGEM DE NOME DE USUÁRIO \_ \_ \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**MODELO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO \_ \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




