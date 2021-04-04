---
title: Habilitando a funcionalidade da Internet
description: Antes de usar as funções WinINet, o aplicativo deve tentar fazer uma conexão com a Internet usando a função InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb44fadaf0726b81618dde19105da7517673a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008031"
---
# <a name="enabling-internet-functionality"></a>Habilitando a funcionalidade da Internet

Antes de usar as funções WinINet, o aplicativo deve tentar fazer uma conexão com a Internet usando a função [**InternetAttemptConnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) . Essa função chama a caixa de diálogo de conexão discada para iniciar uma conexão com a Internet ou verificar se já existe uma conexão. Se essa função falhar, o aplicativo poderá entrar no modo offline, o que permite que ele acesse informações armazenadas em cache durante as conexões anteriores à Internet.

Use a função [**InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) para verificar a conexão com a Internet. Ele tenta executar ping no servidor designado pela URL que é passada para a função. Se o sinalizador SINALIZAr \_ \_ conexão de força ICC \_ estiver definido e a URL for **nula**, a função verificará se há uma entrada no banco de dados do servidor para o servidor mais próximo. Se houver, a função executará ping nesse servidor.

Em seguida, use a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para estabelecer as características da conexão com a Internet que o aplicativo cliente está usando. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) cria o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raiz que é usado para estabelecer sessões [http](http-sessions.md)[FTP](ftp-sessions.md) . O [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) não testa a conexão com a Internet para verificar se as características passadas para a função estão corretas.

Use a função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para criar uma sessão específica. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Inicializa uma sessão para o site especificado usando os argumentos passados a ele e cria um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que é uma ramificação do identificador raiz. O [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) não tenta acessar ou estabelecer uma conexão com o site especificado, exceto no caso de uma sessão de FTP. As funções [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usam o identificador criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para estabelecer uma conexão com o site especificado.

## <a name="using-internetopen"></a>Usando InternetOpen

Para habilitar uma conexão com a Internet, um identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) raiz deve ser criado usando [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Informações sobre o agente do usuário (o aplicativo que chama as funções da Internet), o tipo de acesso à Internet, os nomes de proxy, os hosts e endereços que ignoram o proxy e o comportamento é passado para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Configurando o agente do usuário

O aplicativo de chamada deve fornecer uma cadeia de caracteres que contém o nome do aplicativo ou da entidade acessando a Internet para o parâmetro *lpszAgent* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Essa cadeia de caracteres é usada como o agente do usuário no protocolo HTTP. Por exemplo, o Microsoft Internet Explorer usa o "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Definindo tipos de acesso

O [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) dá suporte a três tipos de acesso:

-   Use INTERNET \_ Open \_ Type \_ Direct se o sistema no qual o aplicativo está sendo executado usar uma conexão direta com a Internet. Os parâmetros *lpszProxyName* e *lpszProxyBypass* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) não são usados e devem ser definidos como **NULL**.
-   Use \_ \_ \_ o proxy de tipo aberto da Internet se o sistema no qual o aplicativo está sendo executado usar um ou mais servidores proxy para acessar a Internet. O [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa os servidores proxy indicados por *lpszProxyName* e ignora o proxy para quaisquer nomes de host ou endereços IP especificados por *lpszProxyBypass*.
-   Use INTERNET \_ Open \_ tipo \_ preconfig para instruir seu aplicativo a recuperar a configuração do registro. Normalmente, essa é a melhor opção, pois a maioria dos aplicativos, incluindo navegadores da Web, usa essa opção.

INTERNET \_ Open \_ Type a \_ preconfig examina os valores de registro **ProxyEnable**, **ProxyServer** e **ProxyOverride**. Esses valores estão localizados em "HKEY \_ Current \_ user \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings".

Se **ProxyEnable** for zero, o aplicativo usará o \_ tipo de abertura direto da Internet \_ \_ . Caso contrário, o aplicativo usará \_ \_ \_ o proxy de tipo aberto da Internet e usará as informações de **ProxyServer** e **ProxyOverride** .

As funções do WinINet fornecerão suporte para proxies de tipo Socks somente se o Internet Explorer estiver instalado. A instalação do Internet Explorer inclui o arquivo Wsock32n.dll, que é necessário para dar suporte a proxies SOCKS. Wsock32n.dll não é redistribuível.

### <a name="listing-proxy-servers"></a>Listando servidores proxy

O WinINet reconhece dois tipos de proxy: proxies de tipo CERN (somente HTTP) e proxies FTP TIS (somente FTP). Se o Internet Explorer estiver instalado, o WinINet também oferecerá suporte a proxies de tipo Socks. O [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) assume, por padrão, que o proxy especificado é um proxy de CERN. Se o tipo de acesso estiver definido como \_ Internet Open \_ Type \_ Direct ou Internet \_ Open \_ Type \_ preconfig, o parâmetro *LpszProxyName* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) deverá ser definido como **null**. Caso contrário, o valor passado para *lpszProxyName* deve conter os proxies em uma cadeia de caracteres delimitada por espaço. As listagens de proxy podem conter o número da porta usado para acessar o proxy.

Para listar um proxy para um protocolo específico, a cadeia de caracteres deve seguir o formato "" <protocol> <protocol> ://<nome do proxy \_> "". Os protocolos válidos são HTTP, HTTPS e FTP. Por exemplo, para listar um proxy de FTP, uma cadeia de caracteres válida seria "" FTP = FTP://FTP \_ proxy \_ Name: 21 "", onde \_ \_ o nome do proxy FTP é o nome do proxy FTP e 21 é o número da porta que deve ser usado para acessar o proxy. Se o proxy usar o número da porta padrão para esse protocolo, o número da porta poderá ser omitido. Se um nome de proxy estiver listado por si só, ele será usado como o proxy padrão para qualquer protocolo que não tenha um proxy específico especificado. Por exemplo, "" http = https://http\_proxy other "" usaria o \_ proxy http para qualquer operação http, enquanto todos os outros protocolos usariam outros.

Por padrão, a função pressupõe que o proxy especificado por *lpszProxyName* seja um proxy de CERN. Um aplicativo pode especificar mais de um proxy, incluindo proxies diferentes para os diferentes protocolos. Por exemplo, se você especificar "" FTP = FTP://FTP-GW HTTP = https://jericho:99 proxy "", as solicitações de FTP serão feitas por meio do proxy de FTP-GW, que escuta na porta 21, e as solicitações HTTP são feitas por meio de um proxy CERN chamado Jericho, que escuta na porta 99. Caso contrário, as solicitações HTTP seriam feitas por meio do proxy CERN chamado proxy, que escuta na porta 80. Observe que, se o aplicativo estiver usando apenas o FTP, por exemplo, ele não precisará especificar "" FTP = FTP://FTP-GW: 21 "". Ele poderia especificar apenas "" FTP-GW "". Um aplicativo só será necessário para especificar os nomes de protocolo se ele estiver usando mais de um protocolo por identificador retornado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Listando o bypass do proxy

Os nomes de host ou endereços IP que não devem ser enviados ao proxy podem ser listados na lista de bypass de proxy. Essa lista pode conter curingas, " \* ", que fazem com que o aplicativo ignore o servidor proxy para endereços que se ajustam ao padrão especificado. Para listar vários endereços e nomes de host, separe-os com ponto e vírgula na cadeia de caracteres de bypass de proxy. Se a <local> macro "" for especificada, a função ignorará o proxy para qualquer nome de host que não contenha um ponto.

Por padrão, o WinINet irá ignorar o proxy para solicitações que usam os nomes de host "localhost", "Loopback", "127.0.0.1" ou " \[ :: 1 \] ". Esse comportamento existe porque um servidor proxy remoto normalmente não resolverá esses endereços corretamente.

**Internet Explorer 9:** Você pode remover o computador local da lista de bypass de proxy usando a macro "<-loopback>".

O exemplo a seguir mostra chamadas de exemplo para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usando diferentes cadeias de caracteres de bypass de proxy. Os comentários acima de cada chamada descrevem o efeito que a cadeia de caracteres de bypass tem nos nomes de host que são acessados do identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que ele cria.


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>Usando InternetConnect

Para iniciar uma sessão, a função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve criar um identificador fora do identificador raiz retornado pela função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) define o endereço do servidor, o número da porta, o nome de usuário, a senha e o tipo de serviço.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raiz criado pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) para estabelecer um identificador de sessão. Se o [sinalizador \_ \_ assíncrono de sinalizador da Internet](api-flags.md) tiver sido definido na chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deverá incluir um valor de contexto diferente de zero.

O nome do servidor pode conter o nome do host (por exemplo, "www.servername.com") ou o número de IP do site no formato ASCII pontilhado-decimal (por exemplo, "10.0.1.45").

A porta do servidor é o número da porta TCP/IP (protocolo de controle de transmissão/protocolo Internet) ao qual se conectar no servidor. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usará a porta padrão para o tipo de serviço selecionado se o \_ valor de número de porta inválido da Internet \_ \_ for usado. As tabelas a seguir contêm os padrões de porta do servidor para o WinINet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>INTERNET_DEFAULT_FTP_PORT</td>
<td>Use a porta padrão para servidores FTP (porta 21).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_GOPHER_PORT</td>
<td>Use a porta padrão para servidores Gopher (porta 70).
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Use a porta padrão para servidores http (porta 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Use a porta padrão para servidores HTTPS (porta 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Use a porta padrão para servidores de firewall Socks (porta 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definindo o nome de usuário e a senha

O valor de *lpszUsername* é o endereço de uma cadeia de caracteres terminada em **nulo** que contém o nome do usuário que está fazendo logon. Se esse parâmetro for **nulo**, a função usará um padrão apropriado, exceto para http. Um parâmetro **nulo** em http faz com que o servidor retorne um erro. Para o protocolo FTP, o padrão é anônimo.

O valor de *lpszPassword* é o endereço de uma cadeia de caracteres terminada em **nulo** que contém a senha de logon. Se *lpszUsername* e *lpszPassword* forem **nulos**, a função usará a senha anônima padrão. No caso do FTP, a senha anônima padrão é o nome de email do usuário. Se *lpszUsername* não for **nulo** e *lpszPassword* for **nulo**, a função usará uma senha em branco. Há quatro configurações possíveis de *lpszUsername* e *lpszPassword*, que produzem os comportamentos mostrados na tabela a seguir.



| *lpszUsername*      | *lpszPassword*      | Nome de usuário enviado ao servidor FTP | Senha enviada ao servidor FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | modo                  | Nome de email do usuário           |
| Cadeia de caracteres não **nula** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Cadeia de caracteres não **nula** | ERROR                        | ERROR                       |
| Cadeia de caracteres não **nula** | Cadeia de caracteres não **nula** | *lpszUsername*               | *lpszPassword*              |



 

Essas informações podem ser alteradas usando as funções [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) . [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) altera os valores de nome de usuário e senha, enquanto [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) exibe uma caixa de diálogo que solicita o nome de usuário e a senha apropriados.

### <a name="defining-the-session"></a>Definindo a sessão

Para definir a sessão que está sendo estabelecida, defina o tipo de serviço, os sinalizadores e o valor de contexto para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

Há dois tipos de serviço disponíveis para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta): serviço de Internet \_ \_ FTP e Internet \_ Service \_ http. \_ \_ O http do serviço de Internet é usado para sessões http e HTTPS.

[Internet \_ O sinalizador \_ passivo](api-flags.md) é o único sinalizador específico de serviço usado pelas funções Wininet. Esse sinalizador pode ser definido quando o tipo de serviço for INTERNET \_ Service \_ FTP para usar a semântica de FTP passiva.

Para todas as operações síncronas, o valor de *dwContext* deve ser definido como zero. Se as operações assíncronas tiverem sido estabelecidas com a definição do sinalizador [ \_ \_ assíncrono de sinalizador da Internet](api-flags.md) na chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), um valor diferente de zero deverá ser fornecido para *dwContext*. Para obter mais informações sobre operações assíncronas, consulte [Configurando operações assíncronas](common-functions.md).

Para sessões de FTP, o [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) tenta estabelecer uma conexão com o servidor na Internet. Para sessões HTTP, o [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) não estabelece uma conexão até que outra função tente obter informações do servidor.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

