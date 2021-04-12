---
title: Visão geral de segurança
description: A estrutura de segurança na API de serviços Web do Windows (WWSAPI) fornece integridade de mensagem, confidencialidade, detecção de repetição e autenticação de servidor usando a segurança de transporte.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Visão geral de segurança dos serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454228"
---
# <a name="security-overview"></a>Visão geral de segurança

A estrutura de segurança na API dos serviços Web do Windows (WWSAPI) fornece:

-   Integridade da mensagem, confidencialidade, detecção de repetição e autenticação de servidor usando a segurança de transporte.
-   Autenticação de cliente, como validação de token de segurança, confiança de certificado e verificações de revogação, etc usando segurança de mensagem SOAP ou segurança de transporte.

## <a name="the-security-programming-model"></a>O modelo de programação de segurança

A segurança está associada a [canais de comunicação](channel-layer-overview.md). A proteção de um canal consiste nas etapas a seguir.

-   Crie e inicialize uma ou mais [**associações de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) apropriadas para os requisitos de segurança do aplicativo.
-   Crie uma [**Descrição de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contenha essas associações de segurança.
-   Crie um [**proxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) de [**canal**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) ou de serviço (no lado do cliente) ou crie um [**ouvinte**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) ou um [**host de serviço**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (no lado do servidor) passando essa descrição de segurança.
-   Execute as etapas de programação de canal normal de abrir, aceitar, enviar, receber, fechar etc.

As mensagens enviadas e recebidas no canal são protegidas automaticamente pelo tempo de execução de acordo com a descrição de segurança fornecida. Opcionalmente, essas etapas podem ser ajustadas especificando uma ou mais configurações de [segurança de todo o canal](security-channel-settings.md) na descrição de segurança ou nas [configurações de segurança de toda a ligação](security-binding-settings.md) em uma associação de segurança.

Qualquer autorização necessária de identidades de remetente deve ser feita pelo aplicativo usando os [resultados de processamento de segurança](security-processing-results.md) anexados a cada mensagem recebida. As etapas de autorização não são especificadas na descrição de segurança, nem são executadas automaticamente pelo tempo de execução.

Erros na descrição de segurança, como associações sem suporte, campos/propriedades inaplicáveis, falta de propriedades/campos obrigatórios ou valores de propriedade/campo inválidos, causarão falha na criação do canal ou do ouvinte.

## <a name="selecting-security-bindings"></a>Selecionando associações de segurança

Ao projetar a segurança de um aplicativo, a decisão principal é a seleção das associações de segurança a serem incluídas na descrição de segurança. Veja a seguir algumas diretrizes para escolher as associações de segurança adequadas para o cenário de segurança de um aplicativo. Uma heurística útil é primeiro entender quais tipos de credenciais de segurança (como [**certificados X. 509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), [**nome de usuário/senhas de domínio do Windows**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential), [**nome de usuário/senhas definidos pelo aplicativo**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)) estarão disponíveis para o aplicativo e, em seguida, escolha uma associação de segurança que possa usar esse tipo de credencial.

-   Segurança de transporte, em que a segurança é aplicada no nível de fluxo de bytes de transporte (abaixo dos limites de mensagem SOAP), é a primeira opção a ser considerada.
    -   Para cenários da Internet e para os cenários de intranet em que um certificado X. 509 pode ser implantado no servidor, o aplicativo pode usar a [**\_ Associação de segurança de \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). O exemplo a seguir ilustra essa opção. Cliente: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

        Se a autenticação de cliente via autenticação de cabeçalho HTTP for desejada, uma [**Associação de segurança de \_ \_ autenticação de cabeçalho \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) poderá ser adicionada para fornecer essa funcionalidade.

    -   Para cenários de intranet em que os protocolos de autenticação integrada do Windows, como Kerberos, NTLM e SPNEGO, são apropriados, o aplicativo pode usar a [**Associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). O exemplo a seguir ilustra essa opção: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Cliente sobre pipes nomeados: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Servidor sobre pipes nomeados: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Para cenários de máquina local em que os protocolos de autenticação integrada do Windows, como Kerberos, NTLM e SPNEGO, são apropriados, o aplicativo pode usar a associação de [**segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) ou a associação de [**\_ \_ \_ \_ segurança \_ de transporte SSPI do WS NAMEDPIPE**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). A [**\_ Associação de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) é preferida nesses cenários, pois garante que o tráfego não sairá da máquina (essa é a propriedade da **\_ Associação de \_ canal \_ do WS NAMEDPIPE**).

-   Segurança de modo misto, em que a segurança de transporte protege a conexão e um cabeçalho de WS-Security na mensagem SOAP fornece autenticação de cliente, é a próxima opção a ser considerada. As associações a seguir são usadas em conjunto com uma das associações de segurança de transporte descritas na seção anterior.
    -   Quando o cliente é autenticado por um par de nome de usuário/senha no nível de aplicativo, o aplicativo pode usar uma [**Associação de segurança de mensagem de nome de \_ usuário \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) para fornecer os dados de autenticação. Os exemplos a seguir ilustram o uso dessa associação em conjunto com [**uma \_ \_ Associação de \_ segurança \_ de transporte WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding):
        -   Cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Quando o cliente é autenticado por um tíquete Kerberos, o aplicativo pode usar uma [**\_ Associação de \_ \_ segurança de \_ \_ mensagem APREQ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) para fornecer os dados de autenticação.
    -   Ao usar um [contexto de segurança](security-context.md), o cliente primeiro estabelece um contexto de segurança com o servidor e, em seguida, usa esse contexto para autenticar mensagens. Para habilitar essa funcionalidade, a descrição de segurança deve conter [**uma \_ \_ Associação de \_ \_ segurança de \_ mensagem de contexto de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Depois de estabelecidas, os contextos de segurança podem ser transmitidos por meio de tokens leves, o que evita que você precise enviar as credenciais de cliente potencialmente grandes e computacionalmente caras com cada mensagem.
    -   Em um cenário de [segurança federada](federation.md) , o cliente primeiro obtém um token de segurança emitido por um serviço de token de segurança (STS) e, em seguida, apresenta o token emitido para um serviço. No lado do cliente: para obter o token de segurança do STS, o aplicativo pode usar [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). Como alternativa, o aplicativo pode usar uma biblioteca do provedor de token de segurança do lado do cliente, como o CardSpace ou o LiveID, e então usar a saída para criar localmente um token de segurança usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). De qualquer forma, depois que o token de segurança estiver disponível para o cliente, ele poderá ser apresentado ao serviço usando uma descrição de segurança que contém uma [**Associação de segurança de \_ \_ mensagem de token \_ \_ \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). No lado do servidor: se o token de segurança emitido pelo STS for um token SAML, o servidor poderá usar uma descrição de segurança com [**uma \_ \_ Associação de \_ segurança \_ de mensagem do WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding).
        > [!Note]  
        > Windows 7 e Windows Server 2008 R2: o WWSAPI dá suporte apenas ao [WS-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e ao [WS-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) , conforme definido pelo [perfil de especificação Web Services Security leve (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Para obter detalhes sobre a implementação da Microsoft, consulte a seção de [sintaxe da mensagem](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

         
-   A opção final a ser considerada é usar associações de autenticação sem usar uma associação de proteção, como a [**Associação de segurança de transporte do WS \_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Isso fará com que as credenciais sejam transmitidas em texto não criptografado e possam ter implicações de segurança. O uso dessa opção deve ser avaliado cuidadosamente para garantir que não haja vulnerabilidades como resultado. Um exemplo de uso potencial é a troca de mensagens entre servidores back-end em uma rede privada segura. As configurações a seguir dão suporte a essa opção.

    -   [**WS \_ A \_ \_ Associação de \_ segurança \_ de autenticação de cabeçalho http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) dá suporte a essa opção em todas as configurações.
    -   [**WS \_ A \_ \_ \_ Associação de segurança de mensagem de nome de usuário**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) dá suporte a essa opção no servidor ao usar http como transporte.
    -   [**WS \_ A \_ \_ Associação de \_ segurança \_ de mensagem APREQ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) dá suporte a essa opção no servidor ao usar http como transporte.
    -   [**WS \_ A \_ \_ Associação de \_ segurança \_ de mensagem de contexto de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) dá suporte a essa opção no servidor ao usar http como transporte.
    -   [**WS \_ A \_ \_ \_ Associação de segurança de mensagem SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) dá suporte a essa opção no servidor ao usar http como transporte.

    Habilitar essa opção requer a definição explícita [**do \_ \_ nível de proteção do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) com um valor diferente de **\_ \_ \_ sinal \_ e \_ criptografia de nível de proteção WS**.

## <a name="channels-and-security"></a>Canais e segurança

Conforme observado acima, a segurança tem como escopo os canais. Além disso, as operações de canal são mapeadas para etapas de segurança de forma consistente em todas as associações de segurança.

-   Criação de canal: o conjunto de associações de segurança especificado na descrição de segurança é validado e permanece fixo para o canal posteriormente. A forma da pilha de canais, incluindo quaisquer canais laterais a serem usados para negociações com base em WS-Trust, também é determinada.
-   Abertura de canal: todas as credenciais que são fornecidas como parte das associações de segurança são carregadas e as sessões de segurança são estabelecidas. Em geral, um canal aberto contém o estado de segurança "Live". Abrir um canal de cliente também especifica o endereço do ponto de extremidade do servidor no qual a autenticação do servidor será feita pelo tempo de execução.
-   Entre abrir e fechar o canal: as mensagens podem ser enviadas e recebidas com segurança durante essa fase.
-   Envio de mensagem: tokens de contexto de segurança são obtidos ou renovados conforme necessário e a segurança é aplicada a cada mensagem transmitida de acordo com a descrição de segurança. Erros que são encontrados ao aplicar a segurança são retornados ao aplicativo como erros de envio.
-   Recebimento de mensagem: a segurança é verificada em cada mensagem recebida de acordo com a descrição de segurança. Quaisquer erros de verificação de segurança de mensagem são retornados ao aplicativo como erros de recebimento. Esses erros por mensagem não afetam o estado do canal ou os recebimentos subsequentes. O aplicativo pode descartar um recebimento com falha e reiniciar um recebimento para outra mensagem.
-   Anulação de canal: o canal pode ser anulado a qualquer momento para interromper toda e/s no canal. Na anulação, o canal entrará em um estado com falha e não permitirá mais envios ou recebimentos. No entanto, o canal ainda pode reter algum estado de segurança "ao vivo", portanto, um fechamento de canal subsequente será necessário para descartar todo o estado corretamente.
-   Fechamento de canal: o estado de segurança criado em aberto é Descartado e as sessões são interrompidas. Tokens de contexto de segurança cancelados. A pilha de canais permanece, mas não contém o estado de segurança ' ao vivo ' ou credenciais carregadas.
-   Canal livre: a pilha de canais criada no Create, junto com todos os recursos de segurança, são liberados.

## <a name="security-apis"></a>APIs de segurança

A documentação da API para segurança é agrupada nos tópicos a seguir.

-   [Descrição de segurança](security-description.md)
    -   [Configurações de canal de segurança](security-channel-settings.md)
    -   [Associações de segurança](security-bindings.md)
        -   [Credenciais de Segurança](security-credentials.md)
        -   [Configurações de associação de segurança](security-binding-settings.md)
-   [Federação](federation.md)
-   [Contexto de segurança](security-context.md)
-   [Identidade de ponto de extremidade](endpoint-identity.md)
-   [Resultados do processamento de segurança](security-processing-results.md)

## <a name="security"></a>Segurança

Ao usar a API de segurança do WWSAPI, os aplicativos enfrentam vários riscos de segurança:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Configuração incorreta acidental
</dt> <dd>

O WWSAPI dá suporte a uma variedade de opções de configuração relacionadas à segurança. Consulte, por exemplo, a [**ID da propriedade de associação de segurança do WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Algumas dessas opções, como a **propriedade de associação de segurança do WS, permitem que \_ \_ \_ \_ \_ \_ clientes anônimos** permitam que o aplicativo reduza o nível padrão de segurança fornecido pelas várias associações de segurança. O uso dessas opções deve ser avaliado cuidadosamente para garantir que não haja vetores de ataque resultantes.

Além disso, conforme descrito acima, o WWSAPI permite que um aplicativo desabilite deliberadamente determinadas etapas necessárias para proteger totalmente uma troca de mensagens, como permitir a desabilitação da criptografia, embora as credenciais de segurança sejam transmitidas. Isso tem permissão para habilitar determinados cenários específicos e não deve ser usado para comunicação geral. O [**\_ \_ nível de proteção do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) deve ser especificamente reduzido para habilitar esses cenários, e os aplicativos não devem alterar esse valor, a menos que seja absolutamente necessário, pois isso desabilitará muitas verificações projetadas para garantir uma configuração segura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Armazenando informações confidenciais na memória
</dt> <dd>

Informações confidenciais, como senhas, que são armazenadas na memória, estão vulneráveis a serem extraídas por um invasor privilegiado por meio de, por exemplo, o arquivo de paginação. O WWSAPI faz uma cópia das credenciais fornecidas e criptografa essa cópia, deixando os dados originais desprotegidos. É responsabilidade do aplicativo proteger a instância original. Além disso, a cópia criptografada é descriptografada brevemente enquanto está sendo usada, abrindo uma janela para extraí-la.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Negação de serviço
</dt> <dd>

O processamento de segurança pode consumir recursos significativos. Cada associação de segurança adicional aumenta esses custos. O WWSAPI anula o processamento de segurança assim que uma falha de verificação de segurança é encontrada, mas algumas verificações, como decisões de autorização, podem não ocorrer até que o trabalho significativo tenha sido executado.

Enquanto uma mensagem é processada no servidor, o estado de segurança é armazenado no heap de mensagem. O aplicativo pode limitar o consumo de memória durante o processamento de segurança, reduzindo o tamanho desse heap por meio das propriedades de heap da propriedade de mensagem do WS \_ \_ \_ \_ . Além disso, determinadas associações de segurança, como a associação de segurança de mensagem de contexto de segurança do WS, \_ \_ \_ \_ \_ podem fazer com que o servidor aloque recursos em nome do cliente. Os limites para esses recursos podem ser configurados por meio dos seguintes valores de [**ID de propriedade de associação de segurança do WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) :

-   \_máximo de \_ \_ \_ \_ \_ \_ \_ contextos pendentes do contexto de segurança da propriedade de associação de segurança do WS
-   \_máximo de \_ \_ \_ \_ \_ \_ \_ contextos ativos do contexto de segurança da propriedade de associação de segurança do WS
-   \_intervalo de \_ \_ renovação do \_ contexto de segurança da propriedade de \_ \_ Associação de \_ segurança WS
-   \_intervalo de \_ \_ \_ \_ \_ sobreposição de contexto de segurança da propriedade \_ de associação de segurança WS

Definir esses limites como valores baixos reduz o consumo máximo de memória, mas pode levar a clientes legítimos sendo rejeitados quando a cota for atingida.

</dd> </dl>

 

 