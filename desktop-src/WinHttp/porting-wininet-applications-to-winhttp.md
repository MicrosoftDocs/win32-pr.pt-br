---
description: O Microsoft Windows Http Services (WinHTTP) é direcionado a aplicativos de servidor de camada intermediária e back-end que exigem acesso a uma pilha de clientes HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Portando aplicativos WinINet para WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052004"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Portando aplicativos WinINet para WinHTTP

O Microsoft Windows Http Services (WinHTTP) é direcionado a aplicativos de servidor de camada intermediária e back-end que exigem acesso a uma pilha de clientes HTTP. [O Microsoft Windows Internet (WinINet)](winhttp-start-page.md) fornece uma pilha de clientes HTTP para aplicativos cliente, bem como acesso aos protocolos protocolo FTP (FTP), SOCKSv4 e Gopher. Esta visão geral pode ajudar a determinar se a portação de seus aplicativos WinINet para WinHTTP seria benéfica. Ele também descreve requisitos de conversão específicos.

-   [Coisas a considerar antes de portar seu aplicativo WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Equivalentes de WinHTTP para funções WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Tratamento diferente de solicitações assíncronas](#different-handling-of-asynchronous-requests)
-   [Diferenças nas notificações de retorno de chamada do WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Diferenças de autenticação](#authentication-differences)
-   [Diferenças em transações HTTP seguras](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Coisas a considerar antes de portar seu aplicativo WinINet

Considere a possibilidade de portar seu aplicativo WinINet para WinHTTP se o aplicativo se beneficiar de:

-   Uma pilha de clientes HTTP segura para servidor.
-   Uso de pilha minimizado.
-   A escalabilidade de um aplicativo de servidor.
-   Menos dependências em APIs relacionadas à plataforma.
-   Suporte para representação de thread.
-   Uma pilha HTTP amigável ao serviço.
-   Acesso ao objeto [**WinHttpRequest**](winhttprequest.md) com script.

Não considere a porta de seu aplicativo WinINet para WinHTTP se ele deve dar suporte a um ou mais dos seguintes:

-   O protocolo FTP ou Gopher da pilha HTTP.
-   Suporte para protocolo SOCKSv4 para comunicação com proxies SOCKS.
-   Serviços de discagem automática.

Se você decidir porportar seu aplicativo para WinHTTP, as seções a seguir orientarão você pelo processo de conversão.

Para um aplicativo de exemplo para WinINet e WinHTTP, compare o exemplo AsyncDemo para WinINet com o exemplo AsyncDemo para WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Equivalentes de WinHTTP para funções WinINet

A tabela a seguir lista as funções WinINet relacionadas à pilha de clientes HTTP junto com os equivalentes de WinHTTP.

Se o seu aplicativo exigir funções WinINet que não estão listadas, não porte seu aplicativo para WinHTTP.



| Função WinINet                                                       | Equivalente a WinHTTP                                                                                                                                                                                     | Alterações importantes                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | O valor de contexto é definido [**com WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). As opções de solicitação são definidas [**com WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) deve ser chamado depois de enviar uma solicitação.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | O valor de contexto é definido [**com WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | O valor de contexto pode ser definido com [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Buffers não podem ser fornecidos.                                                                                                                                                                                                                                                                                                          |
| [**Internetcanonicalizeurl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Sem equivalente                                                                                                                                                                                          | As URLs agora são colocadas em formato canônico [**em WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Sem equivalente                                                                                                                                                                                          | Não implementado no WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | Fechar um alça pai no WinHTTP não fecha recursivamente os alças filho.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Sem equivalente                                                                                                                                                                                          | As URLs podem ser montadas com a [**função WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Sem equivalente                                                                                                                                                                                          | Não implementado no WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**Internetconnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | O valor de contexto é definido [**com WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). As opções de solicitação são definidas [**com WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) As credenciais do usuário são definidas [**com WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportamento oposto do sinalizador ESCAPE de ICU: com InternetCrackUrl, esse sinalizador faz com que sequências de escape (%xx) sejam convertidas em caracteres, mas com \_ [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), faz com que os caracteres que devem ser escapados de em uma solicitação HTTP sejam convertidos em sequências de escape. [](/windows/desktop/api/wininet/nf-wininet-internetcrackurla) |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Sem equivalente                                                                                                                                                                                          | Como o WinHTTP é direcionado a aplicativos do lado do servidor, ele não implementa nenhuma interface do usuário.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Sem equivalente                                                                                                                                                                                          | O WinHTTP não persiste dados entre sessões e não pode acessar cookies winINet.                                                                                                                                                                                                                                                    |
| [**InternetA abrir**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**Internetopenurl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Essa funcionalidade está disponível nas funções WinHTTP listadas.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Nenhum parâmetro reservado.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | O WinHTTP oferece um conjunto diferente de opções do WinINet. Para obter mais informações e opções oferecidas pelo WinHTTP, consulte [**Sinalizadores de opção**](option-flags.md).                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Em vez de uma estrutura, o buffer é uma região de memória endereçada com um ponteiro.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Para obter mais informações, consulte "manipulação diferente de solicitações assíncronas" neste tópico.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Nenhum.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Nenhum.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Manipulação diferente de solicitações assíncronas

Lembre-se de que no WinINet e no WinHTTP, algumas funções podem concluir solicitações assíncronas de forma síncrona ou assíncrona. Seu aplicativo deve lidar com qualquer situação. Há diferenças significativas em como o WinINet e o WinHTTP tratam dessas funções potencialmente assíncronas.

WinINet

-   Conclusão síncrona: se uma chamada de função WinINet potencialmente assíncrona for concluída de forma síncrona, os parâmetros de saída da função retornarão os resultados da operação. Quando ocorrer um erro, recupere o código de erro chamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) após a chamada de função WININET.

-   Conclusão assíncrona: se uma chamada de função potencialmente assíncrona for concluída de modo assíncrono, os resultados da operação e de quaisquer erros poderão ser acessados na função de retorno de chamada. A função de retorno de chamada é executada em um thread de trabalho, não no thread que fez a chamada de função inicial.

Em outras palavras, seu aplicativo deve duplicar a lógica para lidar com os resultados dessas operações em dois locais: ambos imediatamente após a chamada de função e na função de retorno de chamado.

O WinHTTP simplifica esse modelo, permitindo que você implemente a lógica operacional somente na função de retorno de chamada, que recebe uma notificação de conclusão, independentemente de a operação ser concluída de forma síncrona ou assíncrona. Quando a operação assíncrona está habilitada, os parâmetros de saída das funções do WinHTTP não retornam dados significativos e devem ser definidos como **NULL**.

A única diferença significativa entre a conclusão assíncrona e síncrona no WinHTTP, da perspectiva do aplicativo, é em que a função de chamada de retorno é executada.

WinHTTP

-   Conclusão síncrona: quando uma operação é concluída de forma síncrona, os resultados são retornados em uma função de retorno de chamada que é executada no mesmo thread que a chamada de função original.

-   Conclusão assíncrona: quando uma operação é concluída de forma assíncrona, os resultados são retornados em uma função de retorno de chamada que é executada em um thread de trabalho.

Embora a maioria dos erros também possa ser manipulada inteiramente na função de retorno de chamada, os aplicativos WinHTTP ainda devem estar preparados para que uma função retorne **false** devido a um parâmetro de erro \_ inválido \_ ou a outro erro semelhante recuperado chamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Ao contrário do WinINet, que pode executar várias operações assíncronas simultaneamente, o WinHTTP impõe uma política de uma operação assíncrona pendente por identificador de solicitação. Se uma operação estiver pendente e outra função WinHTTP for chamada, a segunda função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ operação inválida \_ .

O WinHTTP simplifica esse modelo, permitindo que você implemente a lógica operacional somente na função de retorno de chamada, que recebe uma notificação de conclusão, independentemente de a operação ser concluída de forma síncrona ou assíncrona. Quando a operação assíncrona está habilitada, os parâmetros de saída das funções do WinHTTP não retornam dados significativos e devem ser definidos como **NULL**.

## <a name="differences-in-winhttp-callback-notifications"></a>Diferenças nas notificações de retorno de chamada do WinHTTP

A função de retorno de chamada de status recebe atualizações sobre o status das operações por meio de sinalizadores de notificação. No WinHTTP, as notificações são selecionadas usando o parâmetro *dwNotificationFlags* da função [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) . Use o sinalizador **sinalizador de retorno de chamada do WinHTTP \_ \_ \_ todas as \_ notificações** para ser notificado de todas as atualizações de status.

As notificações que indicam que uma operação específica está concluída são chamadas de notificações de conclusão ou apenas conclusões. No WinINet, cada vez que a função de retorno de chamada recebe uma conclusão, o parâmetro *lpvStatusInformation* contém uma estrutura de [**\_ \_ resultados assíncronos da Internet**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) . No WinHTTP, essa estrutura não está disponível para todas as conclusões. É importante examinar a página de referência para o [**\_ retorno de \_ chamada de status do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback), que contém informações sobre notificações e quais tipos de dados podem ser esperados para cada um.

No WinHTTP, uma única conclusão, **\_ erro de \_ \_ solicitação de \_ status de retorno de chamada WinHTTP**, indica que uma operação falhou. Todas as outras conclusões indicam uma operação bem-sucedida.

O WinINet e o WinHTTP usam um valor de contexto definido pelo usuário para passar informações do thread principal para a função de retorno de chamada de status, que pode ser executada em um thread de trabalho. No WinINet, o valor de contexto usado pela função de retorno de chamada de status é definido chamando uma das várias funções. No WinHTTP, o valor de contexto é definido somente com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Por isso, é possível no WinHTTP que uma notificação ocorra antes que um valor de contexto seja definido. Se a função de retorno de chamada receber uma notificação antes de o valor do contexto ser definido, o aplicativo deverá estar preparado para receber **nulo** no parâmetro *dwContext* da função de retorno de chamada.

## <a name="authentication-differences"></a>Diferenças de autenticação

No WinINet, as credenciais do usuário são definidas chamando a função [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) , usando um código semelhante ao fornecido no exemplo de código a seguir.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Para compatibilidade, as credenciais de usuário podem ser definidas de forma semelhante no WinHTTP usando a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , mas isso não é recomendado porque pode representar uma vulnerabilidade de segurança.

Em vez disso, quando um aplicativo recebe um código de status 401 no WinHTTP, o método recomendado de configuração de credenciais é primeiro para identificar um esquema de autenticação usando [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) e, segundo, definir as credenciais usando [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). O exemplo de código a seguir mostra como fazer isso.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Como não há nenhum equivalente a [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) no WinHTTP, os aplicativos que obtêm credenciais por meio de uma interface do usuário devem fornecer sua própria interface.

Ao contrário do WinINet, o WinHTTP não armazena senhas em cache. Credenciais de usuário válidas devem ser fornecidas para cada solicitação.

O WinHTTP não dá suporte ao esquema de autenticação de senha distribuída (DPA) suportado pelo WinINet. No entanto, o WinHTTP oferece suporte a Microsoft Passport 1,4. Para obter mais informações sobre como usar a autenticação do Passport no WinHTTP, consulte [autenticação do Passport no WinHTTP](passport-authentication-in-winhttp.md).

O WinHTTP não depende das configurações do Internet Explorer para determinar a política de logon automática. Em vez disso, a política de logon automático é definida com [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Para obter mais informações sobre autenticação no WinHTTP, incluindo a política de logon automático, consulte [autenticação no WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Diferenças em transações HTTP seguras

No WinINet, inicie uma sessão segura usando [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) ou [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), mas no WinHTTP, você deve chamar [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) usando o sinalizador **de \_ \_ segurança sinalizador do WinHTTP** .

Em uma transação HTTP segura, os certificados de servidor podem ser usados para autenticar um servidor no cliente. No WinINet, se um certificado de servidor contiver erros, [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) falhará e fornecerá detalhes sobre os erros de certificado.

No WinHttp, os erros de certificado do servidor são tratados de acordo com a versão da seguinte maneira:

-   A partir do WinHttp 5,1, se um certificado de servidor falhar ou contiver erros, a chamada para [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) relatará uma **\_ \_ \_ \_ falha segura de status de retorno de chamada de WinHTTP** na função de retorno de chamada. Se o erro gerado por **WinHttpSendRequest** for ignorado, as chamadas subsequentes para [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) falharão com um erro de \_ operação de WinHTTP \_ \_ cancelada.
-   No WinHTTP 5,0, os erros nos certificados de servidor não, por padrão, causam uma falha na solicitação. Em vez disso, os erros são relatados na função de retorno de chamada com a notificação de **\_ \_ \_ \_ falha segura de status de retorno de chamada WinHTTP** .

em algumas plataformas anteriores, o WinINet suportava os protocolos PCT (tecnologia de comunicação privada) e/ou Fortezza, embora não no Windows XP.

O WinHTTP não dá suporte aos protocolos PCT e Fortezza em nenhuma plataforma e, em vez disso, depende de protocolo SSL (SSL) 2,0, SSL 3,0 ou TLS (Transport Layer Security) 1,0.

 

 
