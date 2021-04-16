---
title: Federação
description: A Federação permite a delegação de autoridade de autorização para outros membros de um Interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Serviços Web de Federação para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104563259"
---
# <a name="federation"></a>Federação

A Federação permite a delegação de autoridade de autorização para outros membros de um Interprise. Por exemplo, considere o seguinte problema de negócios: a empresa de fabricação de peças auto Ltd deseja permitir que funcionários autorizados de seu cliente Fabrikam Inc acessem com segurança o serviço Web de pedidos de peças da contoso. Uma solução de segurança para esse cenário é que a contoso configure um mecanismo de confiança com a Fabrikam para delegar a decisão de autorização de acesso à fabrikam. Esse processo pode funcionar da seguinte maneira:

-   A Fabrikam, quando se torna um parceiro da Contoso, configura um contrato de confiança com a contoso. O objetivo desta etapa é concordar com o tipo de token de segurança e o conteúdo que representará a autorização da Fabrikam e será aceitável para a contoso. Por exemplo, pode ser decidido que um certificado X. 509 confiável com o nome da entidade "CN = Fabrikam Inc Supplier STS" deve assinar um token SAML para que o SAML seja aceito pelo serviço Web da contoso. Além disso, pode ser decidido que a declaração de segurança no token SAML emitido deve ser ' https://schemas.contoso.com/claims/lookup ' (para autorização de pesquisa de parte) ou ' https://schemas.contoso.com/claims/order ' (para autorização de ordenação de partes).
-   Quando um funcionário da Fabrikam usa o aplicativo de ordenação de partes internas, ele primeiro entra em contato com um serviço de token de segurança (STS) dentro da Fabrikam. Esse funcionário é autenticado usando o mecanismo de segurança interno da Fabrikam (digamos, nome de usuário do domínio do Windows/senha), sua autorização para ordenar partes é verificada e recebe um token SAML de curta duração que contém as declarações apropriadas e assinado pelo certificado X. 509 decidido acima. O aplicativo de ordenação de peças, em seguida, contata o serviço contoso, apresentando o token SAML emitido para autenticar e executar a tarefa de ordenação.

Aqui, o STS da Fabrikam atua como "parte emissora" e o serviço de peças da Contoso atua como "terceira parte confiável". ![Diagrama mostrando uma parte emissora e uma terceira parte confiável em uma federação.](images/stsmodel.png)

## <a name="federation-features"></a>Recursos de Federação

Veja a seguir os recursos de segurança com suporte para as partes ou funções envolvidas em um cenário de Federação:

-   No lado do cliente: para obter o token de segurança do STS, é possível usar a função [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) . Como alternativa, é possível usar uma biblioteca do provedor de token de segurança do lado do cliente, como o CardSpace ou o LiveID, e usar a saída para criar localmente um token de segurança usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). De qualquer forma, depois que o cliente tiver o token de segurança, ele poderá criar um canal para o serviço especificando a [**Associação de segurança de \_ \_ mensagem de token \_ \_ \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) para apresentar o token, junto com uma associação de segurança de transporte, como a [**\_ \_ \_ \_ Associação de segurança de transporte WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger o canal.
-   No lado do servidor: em um cenário de Federação com um serviço de token de segurança que emite tokens SAML, o servidor pode usar a [**\_ Associação de \_ \_ segurança \_ de mensagem SAML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), junto com uma associação de segurança de transporte, como a associação de [**segurança de transporte do WS \_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) para proteger o canal.
-   STS-lado: Observe que o STS é um aplicativo de serviço Web e pode especificar os requisitos de segurança para aqueles que solicitam um token de segurança usando uma estrutura de [**Descrição de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) no momento da criação do ouvinte, assim como qualquer outro serviço Web seguro. Em seguida, ele pode analisar cargas de mensagens de solicitação de entrada para validar as solicitações de token e enviar tokens emitidos de volta como cargas de mensagens de resposta. No momento, nenhum recurso é fornecido para ajudar essas etapas de análise e emissão.

Observe que o lado do cliente pode manipular o token de segurança emitido genericamente como um token de segurança XML sem saber o tipo de token ou fazer o processamento específico do tipo de token. No entanto, o servidor precisa entender o tipo de token de segurança específico para poder entender e processá-lo. As etapas de solicitação e resposta de token de segurança usam as construções definidas na especificação de WS-Trust.

## <a name="more-complex-federation-scenarios"></a>Cenários de Federação mais complexos

Um cenário de Federação pode envolver vários STSs que formam uma cadeia de Federação. Considere o seguinte exemplo:

-   O cliente é autenticado no STS do LiveID usando um nome de usuário/senha do LiveID e Obtém um token de segurança T1.
-   O cliente é autenticado no STS1 usando T1 e Obtém um token de segurança T2.
-   O cliente é autenticado no STS2 usando T2 e Obtém um token de segurança T3.
-   O cliente é autenticado para o serviço de destino usando T3.

Aqui, o STS do LiveID, STS1, STS2 e S formam a cadeia de Federação. O STSs em uma cadeia de Federação pode executar várias funções para o cenário de aplicativo geral. Exemplos de tais funções funcionais do STS incluem provedor de identidade, tomador de decisão de autorização, Anonymizer e Gerenciador de recursos.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parâmetros de solicitação do STS e troca de metadados

Para que o cliente faça uma chamada [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) bem-sucedida, ele precisa saber os parâmetros dessa chamada (como o tipo de token necessário e os tipos de declaração), os requisitos de [**Descrição de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) do canal de solicitação para o STS e o endereço do [ponto de extremidade](endpoint-address.md) do STS. O aplicativo cliente pode usar qualquer uma das seguintes técnicas para determinar essas informações:

-   Codifique as informações no aplicativo como parte das decisões de tempo de design.
-   Leia estas informações de um arquivo de configuração de nível de aplicativo configurado pelo implantador de aplicativos local.
-   Descobrir dinamicamente essas informações em tempo de execução usando o recurso de [importação de metadados](metadata-import.md) com a estrutura de restrição de [**\_ \_ Associação de segurança de mensagem de token \_ \_ \_ \_ emitida do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .

Para ilustrar o uso de MEX dinâmico com Federação, considere o exemplo de 3 STS acima. O cliente primeiro fará um MEX dinâmico com S para obter informações sobre o T3 (ou seja, o que fazer a partir de STS2), bem como o endereço MEX do STS2 Dynamic (ou seja, onde encontrar STS2). Em seguida, ele usará essas informações para fazer um MEX dinâmico com STS2 para descobrir informações sobre T2 e STS1, e assim por diante.

Assim, as etapas de MEX dinâmico ocorrem na ordem 4, 3, 2, 1 para criar a cadeia de Federação e as etapas de solicitação de token e de apresentação ocorrem na ordem 1, 2, 3, 4 para desenrolar a cadeia de Federação.

> [!Note]  
> Windows 7 e Windows Server 2008 R2: o WWSAPI dá suporte apenas ao [WS-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e ao [WS-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) , conforme definido pelo [perfil de especificação Web Services Security leve (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Para obter detalhes sobre a implementação da Microsoft, consulte a seção de [sintaxe da mensagem](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

 

 

 