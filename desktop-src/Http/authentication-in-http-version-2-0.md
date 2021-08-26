---
title: Autenticação (API do servidor HTTP)
description: A partir da versão 2.0, a API do Servidor HTTP executa a autenticação do lado do servidor para o aplicativo.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4e3c35dc4e244fd51af42bb3c52d225d233364f61fc79a8127ef450e84016fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078356"
---
# <a name="authentication-http-server-api"></a>Autenticação (API do servidor HTTP)

Alguns aplicativos de servidor exigem autenticação de cliente para acessar recursos e solicitações HTTP de serviço. A partir da versão 2.0, a API do Servidor HTTP executa a autenticação do lado do servidor para o aplicativo. Na VERSÃO 1.0 da API do Servidor HTTP, o aplicativo de servidor precisava implementar sua própria autenticação. Algumas vantagens da autenticação executada pela API do Servidor HTTP incluem:

-   Os aplicativos podem ser executados com privilégios baixos, reduzindo assim os riscos de segurança.
-   A autenticação é executada no modo kernel, reduzindo assim as transições do modo de usuário para o modo kernel durante a autenticação.
-   A autenticação executada no modo kernel permite que os aplicativos de servidor executem em contas de usuário diferentes. Na versão 1.0, todos os aplicativos no computador devem ser executados na mesma conta de usuário para autenticar no SPN (Nome da Princípio de Serviço).
-   O handshake de autenticação NTLM não será redefinido se um processo de trabalho for reciclado enquanto o handshake estiver em processo.

Para aproveitar a autenticação da versão 2.0, o aplicativo habilita os esquemas de autenticação que a API do Servidor HTTP aplica às URLs para as quais o aplicativo se registrou. A autenticação pode ser habilitada na sessão do servidor ou no grupo de URL. O grupo de URL herdará os esquemas de autenticação habilitados pela sessão do servidor se nenhum estiver definido no grupo de URL. A API do Servidor HTTP dá suporte aos seguintes esquemas:

-   Negotiate
-   NTLM
-   Digest
-   Basic

O aplicativo de servidor também pode implementar esquemas de autenticação sem suporte pela API do servidor HTTP. A API do Servidor HTTP envia solicitações ao aplicativo para esquemas de autenticação sem suporte ou para esquemas que não foram habilitados pelo aplicativo.

### <a name="enabling-authentication"></a>Habilitando autenticação

O aplicativo de servidor habilita e configura a autenticação na sessão do servidor ou no grupo de URL com as funções [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) da seguinte forma:

1.  O aplicativo habilita a autenticação especificando **HttpServerAuthenticationProperty** no parâmetro *Property* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  O aplicativo especifica os parâmetros de configuração na estrutura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) no parâmetro *pPropertyInformation* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) [**ou HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). O aplicativo especifica os esquemas de autenticação habilitados, se o cache de credenciais NTLM está desabilitado e fornece os parâmetros Básico e Digest na estrutura **HTTP \_ SERVER AUTHENTICATION \_ \_ INFO.**

### <a name="authentication-procedure"></a>Procedimento de autenticação

Para iniciar a autenticação do Servidor HTTP, o aplicativo habilita a propriedade de autenticação antes que a primeira solicitação chegue na fila de solicitações. As etapas a seguir são o fluxo de processamento comum para autenticar uma solicitação.

1.  O aplicativo habilita a autenticação. Consulte a seção anterior "Habilitando a autenticação".
    > [!Note]  
    > O cliente envia uma solicitação não autenticada. A API do Servidor HTTP passa a solicitação para o aplicativo de servidor e permite que ela gere o desafio inicial 401. A API do Servidor HTTP inclui a estrutura [**\_ HTTP REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) inserida com a estrutura [**DE \_ SOLICITAÇÃO HTTP.**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) O **membro AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  O aplicativo examina o **membro AuthStatus** da estrutura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar se a solicitação foi autenticada. Se a solicitação não tiver sido autenticada, o aplicativo poderá fazer o serviço da solicitação como anônima ou enviar um desafio inicial de autenticação 401.
3.  Se o aplicativo for o serviço da solicitação como anônimo, ele tratará a solicitação e enviará a resposta final para o aplicativo cliente, assim como se a autenticação não estivesse envolvida.
4.  Se, em vez disso, o aplicativo exigir autenticação, ele enviará o desafio inicial 401 com um ou mais WWW-Authenticate que indicam os esquemas disponíveis para o cliente. O aplicativo deve usar a estrutura [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para criar o conjunto de cabeçalhos necessário quando mais de um cabeçalho de autenticação for enviado na resposta.
    > [!Note]
    >
    > O cliente resende a solicitação com o header de autorização para um esquema selecionado no conjunto de esquemas disponíveis indicado pelo aplicativo de servidor na resposta inicial 401.
    >
    > A API do Servidor HTTP examina o cabeçalho de autorização da solicitação de autorização para determinar se o esquema está habilitado. Se estiver, a API do Servidor HTTP executará a autenticação e manipulará todas as trocas de solicitação/401-resposta provisórios até que o handshake de autenticação seja finalizado.
    >
    > Quando a API do Servidor HTTP conclui a tentativa de autenticação, ela envia a solicitação para o aplicativo com os resultados da tentativa de autenticação na estrutura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) retornada com a solicitação. Se a tentativa de autenticação falhar por um dos seguintes motivos, a API do Servidor HTTP não passará a solicitação para o aplicativo:
    >
    > -   Se o handshake de autenticação falhar devido a um erro interno da API do Servidor HTTP, como uma falha de alocação de memória, a API do Servidor HTTP gerará uma resposta 503 (serviço indisponível) e enviará de volta ao cliente.
    > -   Se um cabeçalho de autorização malformado, como um cabeçalho sem um nome de esquema ou codificação Base64 malformada de credenciais de cliente encontradas, a API do Servidor HTTP gerará uma resposta 400 (solicitação ruim) e enviará de volta ao cliente.

     

5.  O aplicativo de servidor examina o **membro AuthStatus** da estrutura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar se a autenticação foi bem-sucedida. Quando a autenticação falha, a API do Servidor HTTP inclui o erro retornado de [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) no membro **SecStatus** da estrutura **HTTP REQUEST \_ \_ AUTH \_ INFO.** Se a tentativa de autenticação falhar devido a credenciais ruins, o aplicativo poderá gerar outro desafio 401 com o WWW-Authenticate desejado ou poderá decidir a manutenção da solicitação como anônima.
6.  Se a autenticação tiver sido bem-sucedida, o aplicativo usará o token fornecido na estrutura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para representar o cliente e acessar recursos. O handle de token de acesso retornado ao aplicativo é válido desde que a ID da solicitação seja válida, o que normalmente é até que o aplicativo conclua a resposta à solicitação. No entanto, o token pode expirar durante esse período e o aplicativo pode precisar enviar outro desafio 401 para o cliente.
7.  O aplicativo envia a resposta final 200 OK e deve fechar o alça para o token de acesso.
    > [!Note]  
    > A API do Servidor HTTP anexa os dados de autenticação mútua à resposta final 200 OK, se um tiver sido gerado durante o handshake de autenticação.

     

### <a name="ntlm-null-sessions"></a>Sessões NTLM NULL

Observe que uma sessão NTLM NULL indicada no contexto de segurança final não é tratada como autenticada. Nesse caso, a solicitação é enviada ao aplicativo com um erro HttpAuthStatusFailure na estrutura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) e o aplicativo pode enviar outro desafio 401.

### <a name="preemptive-authentication"></a>Autenticação preemptiva

De acordo com o protocolo HTTP, depois que o cliente estabeleceu a autenticação para um recurso, ele pode enviar preventivamente o cabeçalho de autorização correspondente com solicitações consecutivas subsequentes para o recurso sem aguardar um desafio 401 do servidor. Se o esquema indicado no cabeçalho autorização ainda estiver habilitado pelo aplicativo e tiver suporte da API do Servidor HTTP, o Servidor HTTP tentará a autenticação sem enviar a solicitação para o aplicativo. Quando esse tipo de solicitação autenticada é recebido pelo aplicativo, ele pode optar por descartar a solicitação e regenerar o desafio inicial 401 ou realizar a solicitação como autenticada.

### <a name="mutual-authentication"></a>Autenticação Mútua

Os dados de autenticação mútua são gerados quando o esquema de negociação é usado durante o handshake e são resolvidos para Kerberos e o cliente solicitou autenticação mútua. Os dados de autenticação mútua são inseridos automaticamente pela API do Servidor HTTP na resposta final 200 OK enviada pelo aplicativo de servidor. Por padrão, a API do Servidor HTTP não passa os dados de autenticação mútua para o aplicativo de servidor, pois lida automaticamente com o envio deles. No entanto, se o aplicativo de servidor habilitar o sinalizador ReceiveMutualAuth na estrutura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) na configuração, os dados de autenticação mútua serão passados para o aplicativo na estrutura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) inserida com a SOLICITAÇÃO HTTP autenticada. [**\_**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) Nesse caso, o aplicativo deve enviar os dados de autenticação mútua com a resposta final 200 OK. No caso em que vários sites são atendidos por um único computador, todos os sites no computador usam as credenciais da Conta de Computador Local no domínio para autenticação mútua.

 

 
