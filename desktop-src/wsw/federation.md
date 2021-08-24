---
title: Federação
description: A federação permite a delegação de autoridade de autorização para outros membros de uma interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Serviços Web de Federação para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a902eb9469ad75e8c3c5a283284a009af11bb59b42470c91c39b1f16f83c61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703647"
---
# <a name="federation"></a>Federação

A federação permite a delegação de autoridade de autorização para outros membros de uma interprise. Por exemplo, considere o seguinte problema comercial: a empresa de fabricação de peças automáticas Contoso Ltd gostaria de permitir que os funcionários autorizados de seu cliente Fabrikam Inc acessem com segurança o serviço Web de pedido de peças da Contoso. Uma solução de segurança para esse cenário é a Contoso configurar um mecanismo de confiança com a Fabrikam para delegar a decisão de autorização de acesso à Fabrikam. Esse processo pode funcionar da seguinte forma:

-   A Fabrikam, quando se torna um parceiro da Contoso, configura um contrato de confiança com a Contoso. O objetivo desta etapa é concordar com o tipo de token de segurança e o conteúdo que representará a autorização da Fabrikam e será aceitável para a Contoso. Por exemplo, pode ser decidido que um certificado X.509 confiável com o nome da assunto "CN=Fabrikam Inc Supplier STS" deve assinar um token SAML para que o SAML seja aceito pelo Serviço Web da Contoso. Além disso, pode ser decidido que a declaração de segurança no token SAML emitido deve ser ' ' (para autorização de compra de parte) ou ' ' (para autorização de ordem de https://schemas.contoso.com/claims/lookup https://schemas.contoso.com/claims/order parte).
-   Quando um funcionário da Fabrikam usa o aplicativo de pedidos de partes internas, ele primeiro entra em contato com um STS (serviço de token de segurança) dentro da Fabrikam. Esse funcionário é autenticado usando o mecanismo de segurança interno da Fabrikam (digamos, nome de usuário/senha de domínio do Windows), sua autorização para solicitar partes é verificada e ele é emitido um token SAML de curta duração que contém as declarações apropriadas e assinado pelo certificado X.509 decidido acima. Em seguida, o aplicativo de pedidos de partes contata o serviço Contoso apresentando o token SAML emitido para autenticar e executar a tarefa de ordenação.

Aqui, o STS da Fabrikam atua como a "parte que emana" e o serviço de partes contoso atua como a "parte de confiança". ![Diagrama mostrando uma parte em emissão e uma parte de confiança em uma federação.](images/stsmodel.png)

## <a name="federation-features"></a>Recursos de federação

A seguir estão os recursos de segurança com suporte para as partes ou funções envolvidas em um cenário de federação:

-   Lado do cliente: para obter o token de segurança do STS, é possível usar a [**função WsRequestSecurityToken.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) Como alternativa, é possível usar uma biblioteca de provedores de token de segurança do lado do cliente, como CardSpace ou LiveID, e, em seguida, usar sua saída para criar localmente um token de segurança usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). De qualquer forma, depois que o cliente tiver o token de segurança, ele poderá criar um canal para o serviço especificando ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE TOKEN XML do WS para apresentar o token, junto com uma associação de segurança de transporte, como ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) do [**WS para proteger \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) o canal.
-   Lado do servidor: em um cenário de federação com um serviço de token de segurança que emite tokens SAML, o servidor pode usar a ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM SAML do WS, juntamente com uma associação de segurança de transporte, como A ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) do [**WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)para proteger o canal.
-   StS-side: observe que o STS é um aplicativo de serviço Web e pode especificar [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) os requisitos de segurança para aqueles que solicitam um token de segurança usando uma estrutura de descrição de segurança no momento da criação do ouvinte, assim como qualquer outro serviço Web seguro. Em seguida, ele pode analisar os payloads de mensagem de solicitação de entrada para validar as solicitações de token e enviar tokens emitidos novamente como cargas de mensagem de resposta. Atualmente, nenhum recursos é fornecido para ajudar nessas etapas de análise e emissão.

Observe que o lado do cliente pode manipular o token de segurança emitido genericamente como um token de segurança XML sem saber o tipo de token ou fazer processamento específico do tipo de token. No entanto, o servidor precisa entender o tipo de token de segurança específico para entender e processá-lo. As etapas de solicitação e resposta do token de segurança usam os constructos definidos na especificação WS-Trust segurança.

## <a name="more-complex-federation-scenarios"></a>Cenários de federação mais complexos

Um cenário de federação pode envolver vários STSs que formam uma cadeia de federação. Considere o seguinte exemplo:

-   O cliente é autenticado no LIVEID STS usando um nome de usuário/senha liveID e obtém um token de segurança T1.
-   O cliente é autenticado no STS1 usando T1 e obtém um token de segurança T2.
-   O cliente é autenticado no STS2 usando T2 e obtém um token de segurança T3.
-   O cliente é autenticado no serviço de destino S usando T3.

Aqui, o LiveID STS, STS1, STS2 e S formam a cadeia de federação. Os STSs em uma cadeia de federação podem executar várias funções para o cenário geral do aplicativo. Exemplos dessas funções funcionais sts incluem provedor de identidade, tomadores de decisão de autorização, anonimizador e gerenciador de recursos.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parâmetros de solicitação STS e metadados Exchange

Para que o cliente faça uma chamada [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) bem-sucedida, ele precisa saber os parâmetros dessa [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) chamada (como o tipo de token [](endpoint-address.md) necessário e tipos de declaração), os requisitos de descrição de segurança do canal de solicitação para o STS e o endereço do ponto de extremidade do STS. O aplicativo cliente pode usar qualquer uma das seguintes técnicas para determinar essas informações:

-   Codificar as informações no aplicativo como parte das decisões de tempo de design.
-   Leia essas informações de um arquivo de configuração no nível do aplicativo definido pelo implantador de aplicativo local.
-   Descubra dinamicamente essas informações [](metadata-import.md) em runtime usando o recurso de importação de metadados com a estrutura RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE TOKEN EMITIDO [**\_ \_ \_ \_ \_ \_ PELO WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Para ilustrar o uso do MEX dinâmico com federação, considere o exemplo de 3 STS acima. O cliente primeiro fará um MEX dinâmico com S para obter informações sobre T3 (ou seja, o que perguntar do STS2), bem como o endereço MEX dinâmico STS2 (ou seja, onde encontrar STS2). Em seguida, ele usará essas informações para fazer um MEX dinâmico com STS2 para descobrir informações sobre T2 e STS1 e assim por diante.

Assim, as etapas mex dinâmicas ocorrem na ordem 4, 3, 2, 1 para criar a cadeia de federação e as etapas de solicitação e apresentação de token ocorrem na ordem 1, 2, 3, 4 para desenrolar a cadeia de federação.

> [!Note]  
> Windows 7 e Windows Server 2008 R2: O WWSAPI dá suporte apenas a [Ws-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [Ws-SecureConversation,](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) conforme definido pelo [LWSSP (Lightweight especificação Web Services Security Profile).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Para obter detalhes sobre a implementação da Microsoft, consulte a seção [Sintaxe de MENSAGEM](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) do LWSSP.

 

 

 