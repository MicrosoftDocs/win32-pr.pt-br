---
title: Autenticação (API do servidor HTTP)
description: A partir da versão 2,0, a API do servidor HTTP executa a autenticação do lado do servidor para o aplicativo.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d523df90861c83a45f67811edad243ceee5165
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369108"
---
# <a name="authentication-http-server-api"></a>Autenticação (API do servidor HTTP)

Alguns aplicativos de servidor exigem autenticação de cliente para acessar recursos e solicitações HTTP de serviço. A partir da versão 2,0, a API do servidor HTTP executa a autenticação do lado do servidor para o aplicativo. Na API do servidor HTTP versão 1,0, o aplicativo de servidor tinha que implementar sua própria autenticação. Algumas vantagens da autenticação executada pela API do servidor HTTP incluem:

-   Os aplicativos podem ser executados sob privilégios baixos, reduzindo assim os riscos de segurança.
-   A autenticação é executada no modo kernel, reduzindo assim as transições do modo de usuário para o modo kernel durante a autenticação.
-   A autenticação executada no modo kernel permite que os aplicativos de servidor sejam executados em diferentes contas de usuário. Na versão 1,0, todos os aplicativos no computador devem ser executados na mesma conta de usuário para autenticar o SPN (nome da entidade de serviço).
-   O handshake de autenticação NTLM não será redefinido se um processo de trabalho for reciclado enquanto o handshake estiver em andamento.

Para aproveitar a autenticação da versão 2,0, o aplicativo habilita os esquemas de autenticação que a API do servidor HTTP aplica às URLs para as quais o aplicativo foi registrado. A autenticação pode ser habilitada na sessão do servidor ou no grupo de URLs. O grupo de URLs herdará os esquemas de autenticação habilitados pela sessão de servidor se nenhum estiver definido no grupo de URLs. A API do servidor HTTP dá suporte aos seguintes esquemas:

-   Negotiate
-   NTLM
-   Digest
-   Básico

O aplicativo de servidor também pode implementar esquemas de autenticação não suportados pela API do servidor HTTP. A API do servidor HTTP envia solicitações ao aplicativo para esquemas de autenticação que não têm suporte ou para esquemas que não foram habilitados pelo aplicativo.

### <a name="enabling-authentication"></a>Habilitando autenticação

O aplicativo de servidor habilita e configura a autenticação na sessão do servidor ou no grupo de URLs com as funções [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) da seguinte maneira:

1.  O aplicativo habilita a autenticação especificando **HttpServerAuthenticationProperty** no parâmetro *Property* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  O aplicativo especifica os parâmetros de configuração na estrutura de [**informações de \_ autenticação do servidor \_ \_ http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) no parâmetro *pPropertyInformation* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). O aplicativo especifica os esquemas de autenticação habilitados, se o cache de credenciais NTLM está desabilitado e fornece os parâmetros básico e resumo na estrutura de **\_ informações de \_ autenticação \_ do servidor http** .

### <a name="authentication-procedure"></a>Procedimento de autenticação

Para iniciar a autenticação do servidor HTTP, o aplicativo habilita a propriedade de autenticação antes que a primeira solicitação chegue à fila de solicitações. As etapas a seguir são o fluxo de processamento comum para autenticar uma solicitação.

1.  O aplicativo habilita a autenticação. Consulte a seção "Habilitando a autenticação" anterior.
    > [!Note]  
    > O cliente envia uma solicitação não autenticada. A API do servidor HTTP passa a solicitação para o aplicativo de servidor e permite que ele gere o desafio 401 inicial. A API do servidor HTTP inclui a estrutura de [**\_ informações de \_ autenticação \_ de solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) inserida com a estrutura de [**\_ solicitação HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) . O membro **AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  O aplicativo examina o membro **AuthStatus** da estrutura de [**\_ informações de \_ autenticação \_ de solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar se a solicitação foi autenticada. Se a solicitação não tiver sido autenticada, o aplicativo poderá atender à solicitação como anônima ou enviar um desafio de autenticação inicial 401.
3.  Se o aplicativo serviços de solicitação como anônimo, ele manipulará a solicitação e enviará a resposta final para o aplicativo cliente, como se a autenticação não estivesse envolvida.
4.  Se, em vez disso, o aplicativo exigir autenticação, ele enviará o desafio 401 inicial com um ou mais cabeçalhos de WWW-Authenticate indicando os esquemas disponíveis para o cliente. O aplicativo deve usar a [**estrutura \_ http \_ vários \_ cabeçalhos conhecidos**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para criar o conjunto de cabeçalhos necessário quando mais de um cabeçalho de autenticação é enviado na resposta.
    > [!Note]
    >
    > O cliente reenvia a solicitação com o cabeçalho de autorização para um esquema selecionado do conjunto de esquemas disponíveis indicado pelo aplicativo de servidor na resposta inicial 401.
    >
    > A API do servidor HTTP examina o cabeçalho autorização da solicitação de autorização para determinar se o esquema está habilitado. Se for, a API do servidor HTTP executará a autenticação e tratará todas as trocas de solicitação/401-resposta provisórias até que o handshake de autenticação seja finalizado.
    >
    > Quando a API do servidor HTTP conclui a tentativa de autenticação, ela envia a solicitação para o aplicativo com os resultados da tentativa de autenticação na estrutura de [**\_ informações de \_ autenticação \_ de solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) que é retornada com a solicitação. Se a tentativa de autenticação falhar por um dos motivos a seguir, a API do servidor HTTP não passará a solicitação para o aplicativo:
    >
    > -   Se o handshake de autenticação falhar devido a um erro interno da API do servidor HTTP, como uma falha de alocação de memória, a API do servidor HTTP gerará uma resposta 503 (Serviço indisponível) e enviará de volta para o cliente.
    > -   Se um cabeçalho de autorização malformado, como um cabeçalho sem um nome de esquema, ou uma codificação Base64 malformada de credenciais de cliente for encontrada, a API do servidor HTTP gerará uma resposta 400 (solicitação incorreta) e enviará de volta para o cliente.

     

5.  O aplicativo de servidor examina o membro **AuthStatus** da estrutura [**de \_ \_ \_ informações de autenticação de solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar se a autenticação foi bem-sucedida. Quando a autenticação falha, a API do servidor HTTP inclui o erro retornado de [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) no membro **SecStatus** da estrutura de **informações de \_ \_ autenticação \_ de solicitação HTTP** . Se a tentativa de autenticação falhar devido a credenciais inadequadas, o aplicativo poderá gerar outro desafio de 401 com o cabeçalho de WWW-Authenticate desejado ou poderá decidir atender a solicitação como anônima.
6.  Se a autenticação tiver sido bem-sucedida, o aplicativo usará o token fornecido na estrutura de [**\_ informações de \_ autenticação \_ de solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para representar o cliente e acessar os recursos. O identificador de token de acesso retornado ao aplicativo é válido, desde que a ID da solicitação seja válida, o que normalmente ocorre até que o aplicativo conclua a resposta à solicitação. O token pode, no entanto, expirar durante esse período e o aplicativo pode precisar enviar outro desafio de 401 para o cliente.
7.  O aplicativo envia a resposta final de 200 OK e deve fechar o identificador para o token de acesso.
    > [!Note]  
    > A API do servidor HTTP acrescenta os dados de autenticação mútua à resposta final 200 OK, se um tiver sido gerado durante o handshake de autenticação.

     

### <a name="ntlm-null-sessions"></a>Sessões nulas do NTLM

Observe que uma sessão nula do NTLM indicada no contexto de segurança final não é tratada como autenticada. Nesse caso, a solicitação é enviada ao aplicativo com um erro HttpAuthStatusFailure na estrutura de [**informações de \_ \_ autenticação de \_ solicitação HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) e o aplicativo pode enviar outro desafio 401.

### <a name="preemptive-authentication"></a>Autenticação preemptiva

De acordo com o protocolo HTTP, depois que o cliente tiver estabelecido a autenticação para um recurso, ele poderá enviar preventivamente o cabeçalho de autorização correspondente com solicitações consecutivas subsequentes para o recurso sem esperar por um desafio de 401 do servidor. Se o esquema indicado no cabeçalho Authorization ainda estiver habilitado pelo aplicativo e suportado pela API do servidor HTTP, o servidor HTTP tentará autenticar sem enviar a solicitação ao aplicativo. Quando esse tipo de solicitação autenticada é recebido pelo aplicativo, ele pode optar por descartar a solicitação e gerar novamente o desafio 401 inicial ou atender a solicitação como autenticada.

### <a name="mutual-authentication"></a>Autenticação Mútua

Os dados de autenticação mútua são gerados quando o esquema de negociação é usado durante o handshake e é resolvido para Kerberos, e o cliente solicitou autenticação mútua. Os dados de autenticação mútua são inseridos automaticamente pela API do servidor HTTP na resposta final 200 OK enviada pelo aplicativo do servidor. Por padrão, a API do servidor HTTP não passa os dados de autenticação mútua para o aplicativo de servidor, pois ele manipula automaticamente o envio dele. No entanto, se o aplicativo de servidor habilitar o sinalizador ReceiveMutualAuth na estrutura de [**\_ informações de \_ autenticação \_ do servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) na configuração, os dados de autenticação mútua serão passados para o aplicativo na estrutura de informações de autenticação de [**\_ solicitação \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) inserida com a [**\_ solicitação HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))autenticada. Nesse caso, o aplicativo deve enviar os dados de autenticação mútua com a resposta final de 200 OK. No caso em que vários sites são atendidos por um único computador, todos os sites no computador usam as credenciais da conta do computador local no domínio para autenticação mútua.

 

 
