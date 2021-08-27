---
title: Visão geral de segurança
description: A estrutura de segurança Windows API de Serviços Web (WWSAPI) fornece integridade de mensagem, confidencialidade, detecção de reprodução e autenticação de servidor usando a segurança de transporte.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Visão Geral de Segurança Web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6928afd51ded7104e909994f8b625b931da6a157e859c890066c73074ae7d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089436"
---
# <a name="security-overview"></a>Visão geral de segurança

A estrutura de segurança Windows API de Serviços Web (WWSAPI) fornece:

-   Integridade da mensagem, confidencialidade, detecção de reprodução e autenticação de servidor usando a segurança de transporte.
-   Autenticação de cliente, como validação de token de segurança, confiança de certificado e verificações de revogação, etc. usando segurança de mensagem SOAP ou segurança de transporte.

## <a name="the-security-programming-model"></a>O modelo de programação de segurança

A segurança está associada aos canais [de comunicação](channel-layer-overview.md). Proteger um canal consiste nas etapas a seguir.

-   Crie e inicialize uma ou mais [**vinculações de segurança apropriadas**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) para os requisitos de segurança do aplicativo.
-   Crie uma [**descrição de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contenha essas vinculações de segurança.
-   Crie um canal [**ou**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) [**proxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) de serviço (no lado do cliente) ou crie um ouvinte ou [**host**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) de serviço (no lado do servidor) passando essa descrição de segurança. [](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   Faça as etapas de programação de canal normal de Abrir, Aceitar, Enviar, Receber, Fechar etc.

As mensagens enviadas e recebidas no canal são protegidas automaticamente pelo runtime de acordo com a descrição de segurança fornecida. Opcionalmente, essas etapas podem ser [ajustadas](security-channel-settings.md) especificando uma ou mais configurações [](security-binding-settings.md) de segurança em todo o canal na descrição de segurança ou configurações de segurança em toda a associação em uma associação de segurança.

Qualquer autorização necessária de identidades de remetente deve ser feita pelo aplicativo usando os resultados de [processamento de segurança](security-processing-results.md) anexados a cada mensagem recebida. As etapas de autorização não são especificadas na descrição de segurança nem são executadas automaticamente pelo runtime.

Erros na descrição de segurança, como vinculações sem suporte, propriedades/campos inaplicáveis, falta de propriedades/campos necessárias ou valores inválidos de propriedade/campo, causarão falha na criação de canal ou ouvinte.

## <a name="selecting-security-bindings"></a>Selecionando vinculações de segurança

Ao projetar a segurança para um aplicativo, a decisão principal é a seleção das vinculações de segurança a serem incluídas na descrição de segurança. A seguir estão algumas diretrizes para escolher as vinculações de segurança adequadas para o cenário de segurança de um aplicativo. Uma heurística útil é primeiro entender quais tipos de credenciais de segurança (como [**certificados X.509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), nome de [**usuário/senhas**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)de domínio do Windows , nome de [**usuário/senhas definidos**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)pelo aplicativo ) estarão disponíveis para o aplicativo e, em seguida, escolher uma associação de segurança que possa usar esse tipo de credencial.

-   A segurança de transporte, em que a segurança é aplicada no nível do fluxo de byte de transporte (abaixo dos limites da mensagem SOAP), é a primeira opção a ser considerada.
    -   Para cenários de Internet e para esses cenários de Intranet em que um certificado X.509 pode ser implantado no servidor, o aplicativo pode usar a ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ SSL \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) O exemplo a seguir ilustra essa opção. Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample.](httpserverwithsslexample.md)

        Se a autenticação do cliente por meio da autenticação de cabeçalho HTTP for desejada, uma ASSOCIAÇÃO DE SEGURANÇA DE AUTENTICAÇÃO DE AUTENTICAÇÃO DE CABEÇALHO HTTP do WS poderá ser adicionada para fornecer essa funcionalidade. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)

    -   Para cenários de Intranet em que Windows protocolos de Autenticação Integrada, como Kerberos, NTLM e SPNEGO, são apropriados, o aplicativo pode usar a ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ \_ SSPI TS TSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)do WS . O exemplo a seguir ilustra essa opção: [Client: RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Cliente sobre pipes nomeados: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Servidor sobre pipes nomeados: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Para cenários de computador local em que Windows protocolos de Autenticação Integrada, como Kerberos, NTLM e SPNEGO, são apropriados, o aplicativo pode usar a ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**\_ \_ SSPI TCP \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) do WS ou A ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE [**SSPI DO WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). O [**WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) é preferencial nesses cenários porque garante que o tráfego não saia do computador (essa é a propriedade de **WS \_ NAMEDPIPE CHANNEL \_ \_ BINDING**).

-   A segurança de modo misto, em que a segurança de transporte protege a conexão e um WS-Security na mensagem SOAP fornece autenticação de cliente, é a próxima opção a ser considerada. As seguintes vinculações são usadas em conjunto com uma das vinculações de segurança de transporte descritas na seção anterior.
    -   Quando o cliente é autenticado por um par nome de usuário/senha no nível do aplicativo, o aplicativo pode usar uma ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO do WS para fornecer os dados de autenticação. [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) Os exemplos a seguir ilustram o uso dessa associação em conjunto com uma ASSOCIAÇÃO DE SEGURANÇA DE [**\_ TRANSPORTE SSL \_ \_ \_ do WS:**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
        -   Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Quando o cliente é autenticado por um tíquete Kerberos, o aplicativo pode usar uma ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [**\_ \_ APREQ \_ \_ \_ WS KERBEROS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) para fornecer os dados de autenticação.
    -   Ao usar um [contexto de segurança](security-context.md), o cliente primeiro estabelece um contexto de segurança com o servidor e, em seguida, usa esse contexto para autenticar mensagens. Para habilitar essa funcionalidade, a descrição de segurança deve conter uma ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [**DE CONTEXTO DE SEGURANÇA \_ \_ \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) Depois de estabelecidos, os contextos de segurança podem ser transmitidos por meio de tokens leves, o que evita a precisar enviar as credenciais de cliente potencialmente grandes e computacionalmente caras com cada mensagem.
    -   Em um cenário de segurança [federada,](federation.md) o cliente primeiro obtém um token de segurança emitido por um STS (serviço de token de segurança) e, em seguida, apresenta o token emitido para um serviço. Lado do cliente: para obter o token de segurança do STS, o aplicativo pode usar [**WsRequestSecurityToken.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) Como alternativa, o aplicativo pode usar uma biblioteca de provedores de token de segurança do lado do cliente, como CardSpace ou LiveID, e, em seguida, usar sua saída para criar localmente um token de segurança usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). De qualquer forma, depois que o token de segurança está disponível para o cliente, ele pode ser apresentado ao serviço usando uma descrição de segurança que contém uma ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [**\_ DE TOKEN XML \_ \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) Lado do servidor: se o token de segurança emitido pelo STS for um token SAML, o servidor poderá usar uma descrição de segurança com uma ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM [**\_ SAML \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
        > [!Note]  
        > Windows 7 e Windows Server 2008 R2: O WWSAPI dá suporte apenas a [Ws-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [Ws-SecureConversation,](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) conforme definido pelo [LWSSP (Lightweight especificação Web Services Security Profile).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Para obter detalhes sobre a implementação da Microsoft, consulte a seção [Sintaxe de MENSAGEM](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) do LWSSP.

         
-   A opção final a ser considerada é usar as vinculações de autenticação sem usar uma associação de proteção, como [**WS \_ SSL \_ TRANSPORT SECURITY \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) Isso resultará na transmissão das credenciais em texto não claro e poderá ter implicações de segurança. O uso dessa opção deve ser avaliado cuidadosamente para garantir que não haja vulnerabilidades como resultado. Um exemplo de um possível uso é a troca de mensagens entre servidores de back-end em uma rede privada segura. As configurações a seguir são suportadas por essa opção.

    -   [**WS \_ A \_ ASSOCIAÇÃO DE SEGURANÇA DE \_ \_ \_ AUTENTICAÇÃO DE CABEÇALHO HTTP**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) dá suporte a essa opção em todas as configurações.
    -   [**WS \_ USERNAME \_ MESSAGE SECURITY BINDING \_ \_ dá**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) suporte a essa opção no servidor ao usar HTTP como transporte.
    -   [**WS \_ A ASSOCIAÇÃO DE \_ SEGURANÇA DE MENSAGEM DO KERBEROS APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) dá suporte a essa opção no servidor ao usar HTTP como transporte.
    -   [**WS \_ SECURITY \_ CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ dá**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) suporte a essa opção no servidor ao usar HTTP como transporte.
    -   [**WS \_ A ASSOCIAÇÃO DE \_ SEGURANÇA \_ DE \_ MENSAGEM SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) dá suporte a essa opção no servidor ao usar HTTP como transporte.

    A habilitação dessa opção requer definir explicitamente o NÍVEL de PROTEÇÃO do [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) como um valor diferente de **WS PROTECTION \_ LEVEL SIGN \_ AND \_ \_ \_ ENCRYPT.**

## <a name="channels-and-security"></a>Canais e segurança

Conforme mencionado acima, a segurança está no escopo dos canais. Além disso, as operações de canal mapeiam para etapas de segurança de forma consistente em todas as vinculações de segurança.

-   Criação de canal: o conjunto de vinculações de segurança especificado na descrição de segurança é validado e permanece fixo para o canal depois disso. A forma da pilha de canais, incluindo os canais laterais a serem usados para negociações baseadas em WS-Trust, também é determinada.
-   Canal aberto: todas as credenciais fornecidas como parte das vinculações de segurança são carregadas e as sessões de segurança são estabelecidas. Em geral, um canal aberto contém o estado de segurança "ao vivo". Abrir um canal do cliente também especifica o endereço do ponto de extremidade do servidor em relação ao qual a autenticação do servidor será feita pelo runtime.
-   Entre o canal aberto e o fechamento: as mensagens podem ser enviadas e recebidas com segurança durante essa fase.
-   Envio de mensagem: os tokens de contexto de segurança são obtidos ou renovados conforme necessário e a segurança é aplicada a cada mensagem transmitida de acordo com a descrição de segurança. Os erros encontrados ao aplicar a segurança são retornados ao aplicativo como erros de envio.
-   Recebimento de mensagem: a segurança é verificada em cada mensagem recebida de acordo com a descrição de segurança. Todos os erros de verificação de segurança de mensagem são retornados ao aplicativo como erros de recebimento. Esses erros por mensagem não afetam o estado do canal ou os recebimentos subsequentes. O aplicativo pode descartar um recebimento com falha e reiniciar um recebimento para outra mensagem.
-   Anulação de canal: o canal pode ser anulado a qualquer momento para interromper todas as E/S no canal. Após a anulação, o canal entrará em um estado com falha e não permitirá mais mensagens ou recebimentos. No entanto, o canal ainda pode reter algum estado de segurança "ao vivo", portanto, um fechamento de canal subsequente será necessário para descartar todo o estado corretamente.
-   Fechamento do canal: o estado de segurança criado ao abrir é descartado e as sessões são divididas. Os tokens de contexto de segurança são cancelados. A pilha de canais permanece, mas não contém nenhum estado de segurança 'ao vivo' ou credenciais carregadas.
-   Canal livre: a pilha de canais criada na criação, juntamente com todos os recursos de segurança, é liberada.

## <a name="security-apis"></a>APIs de segurança

A documentação da API para segurança é agrupada nos tópicos a seguir.

-   [Descrição de segurança](security-description.md)
    -   [Canal de segurança Configurações](security-channel-settings.md)
    -   [Vinculações de segurança](security-bindings.md)
        -   [Credenciais de Segurança](security-credentials.md)
        -   [Configurações de associação de segurança](security-binding-settings.md)
-   [Federação](federation.md)
-   [Contexto de segurança](security-context.md)
-   [Identidade de ponto de extremidade](endpoint-identity.md)
-   [Resultados do processamento de segurança](security-processing-results.md)

## <a name="security"></a>Segurança

Ao usar o WWSAPI API de Segurança, os aplicativos enfrentam vários riscos de segurança:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Configuração acidental
</dt> <dd>

O WWSAPI dá suporte a uma variedade de opções de configuração relacionadas à segurança. Veja, por exemplo, [**\_ \_ \_ \_ ID DA PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Algumas dessas opções, como PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA do WS, PERMITEM QUE CLIENTES **\_ \_ \_ \_ \_ ANÔNIMOs \_** permitam que o aplicativo reduza o nível padrão de segurança fornecido pelas várias Vinculações de Segurança. O uso dessas opções deve ser avaliado cuidadosamente para garantir que não haja vetores de ataque resultantes.

Além disso, conforme descrito acima, o WWSAPI permite que um aplicativo desabilite deliberadamente determinadas etapas necessárias para proteger totalmente uma troca de mensagens, como permitir desabilitar a criptografia mesmo que as credenciais de segurança sejam transmitidas. Isso tem permissão para habilitar determinados cenários específicos e não deve ser usado para comunicação geral. O NÍVEL DE PROTEÇÃO do [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) deve ser especificamente inferior para habilitar esses cenários, e os aplicativos não devem alterar esse valor, a menos que seja absolutamente necessário, pois isso desabilitará muitas verificações projetadas para garantir uma configuração segura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Armazenar informações confidenciais na memória
</dt> <dd>

Informações confidenciais, como senhas, armazenadas na memória, são vulneráveis a serem extraídas por um invasor privilegiado por meio do arquivo de página, por exemplo. O WWSAPI faz uma cópia das credenciais fornecidas e criptografa essa cópia, deixando os dados originais desprotegidos. É responsabilidade do aplicativo proteger a instância original. Além disso, a cópia criptografada é brevemente descriptografada durante o uso, abrindo uma janela para extraí-la.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Negação de serviço
</dt> <dd>

O processamento de segurança pode consumir recursos significativos. Cada associação de segurança adicional aumenta esses custos. O WWSAPI anula o processamento de segurança assim que uma falha de verificação de segurança é encontrada, mas determinadas verificações, como decisões de autorização, podem não ocorrer até que um trabalho significativo seja executado.

Enquanto uma mensagem é processada no servidor, o estado de segurança é armazenado no heap de mensagens. O aplicativo pode limitar o consumo de memória durante o processamento de segurança reduzindo o tamanho desse heap por meio de PROPRIEDADES DE \_ HEAP DA PROPRIEDADE DE MENSAGEM do \_ WS. \_ \_ Além disso, determinadas vinculações de segurança, como a ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do WS, podem fazer com que o servidor aloce recursos em \_ \_ nome do \_ \_ \_ cliente. Os limites para esses recursos podem ser configurados por meio dos seguintes valores de [**\_ \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) da PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA do WS:

-   CONTEXTOS MÁXIMO PENDENTES DE CONTEXTO DE SEGURANÇA DA PROPRIEDADE DE ASSOCIAÇÃO \_ \_ DE SEGURANÇA DO \_ \_ \_ \_ \_ \_ WS
-   CONTEXTOS ATIVOS MÁXIMOS DE CONTEXTO DE SEGURANÇA DA PROPRIEDADE DE ASSOCIAÇÃO \_ \_ DE SEGURANÇA DO \_ \_ \_ \_ \_ \_ WS
-   INTERVALO DE RENOVAÇÃO DE CONTEXTO DE \_ SEGURANÇA DA PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA \_ \_ \_ \_ \_ \_ DO WS
-   INTERVALO DE ROLLOVER DE CONTEXTO DE \_ SEGURANÇA DA PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA \_ \_ \_ \_ \_ \_ DO WS

Definir esses limites como valores baixos reduz o consumo máximo de memória, mas pode levar a clientes legítimos a serem rejeitados quando a cota é atingida.

</dd> </dl>

 

 