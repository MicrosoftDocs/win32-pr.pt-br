---
title: Manipulando a autenticação
description: Alguns proxies e servidores exigem autenticação antes de conceder acesso aos recursos na Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380850"
---
# <a name="handling-authentication"></a>Manipulando a autenticação

Alguns proxies e servidores exigem autenticação antes de conceder acesso aos recursos na Internet. As funções do WinINet dão suporte à autenticação de servidor e proxy para sessões http. A autenticação de servidores FTP deve ser tratada pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Atualmente, não há suporte para a autenticação de gateway de FTP.

## <a name="about-http-authentication"></a>Sobre a autenticação HTTP

Se a autenticação for necessária, o aplicativo cliente receberá um código de status 401, se o servidor exigir autenticação, ou 407, se o proxy exigir autenticação. Com o código de status, o proxy ou o servidor envia um ou mais cabeçalhos de resposta de autenticação — autenticar proxy (para autenticação de proxy) ou WWW-Authenticate (para autenticação de servidor).

Cada cabeçalho de resposta de autenticação contém um esquema de autenticação disponível e um realm. Se houver suporte para vários esquemas de autenticação, o servidor retornará vários cabeçalhos de resposta de autenticações. O valor do Realm diferenciam maiúsculas de minúsculas e definem um espaço de proteção no proxy ou servidor. Por exemplo, o cabeçalho "WWW-Authenticate: Basic real =" example "" seria um exemplo de um cabeçalho retornado quando a autenticação do servidor for necessária.

O aplicativo cliente que enviou a solicitação pode se autenticar, incluindo um campo de cabeçalho de autorização com a solicitação. O cabeçalho Authorization conterá o esquema de autenticação e a resposta apropriada exigida por esse esquema. Por exemplo, o cabeçalho "Authorization: Basic \<username:password> " seria adicionado à solicitação e enviado novamente ao servidor se o cliente recebeu o cabeçalho de resposta de autenticação "www-Authenticate: Basic Realm =" example "".

Há dois tipos gerais de esquemas de autenticação:

-   Esquema de autenticação básica, em que o nome de usuário e a senha são enviados em texto não criptografado para o servidor.
-   Esquemas de desafio/resposta, que permitem um formato de desafio/resposta.

O esquema de autenticação básica é baseado no modelo que um cliente deve autenticar a si mesmo com um nome de usuário e senha para cada realm. O servidor serviçosá a solicitação se ele for reenviado com um cabeçalho de autorização que inclua um nome de usuário e senha válidos.

Os esquemas de desafio/resposta permitem uma autenticação mais segura. Se uma solicitação exigir autenticação usando um esquema de desafio/resposta, o código de status apropriado e os cabeçalhos de autenticação serão retornados ao cliente. O cliente deve, então, reenviar a solicitação com um Negotiate. O servidor retornaria um código de status apropriado com um desafio e, em seguida, o cliente exigiria reenviar a solicitação com a resposta correta para obter o serviço solicitado.

A tabela a seguir lista os esquemas de autenticação, o tipo de autenticação, a DLL que oferece suporte a eles e uma descrição do esquema.



| Esquema                                    | Type               | DLL                  | Descrição                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto não criptografado)                         | básico              | Wininet.dll          | Usa uma cadeia de caracteres codificada em base64 que contém o nome de usuário e a senha.                                                                                                                                                                                                                                                                             |
| Digest                                    | desafio-resposta | Digest.dll           | Um esquema de desafio/resposta que desafia o uso de um valor nonce (uma cadeia de caracteres de dados especificada pelo servidor). Uma resposta válida contém uma soma de verificação do nome de usuário, a senha, o valor de nonce fornecido, o método HTTP e o Uniform Resource Identifier (URI) solicitado. O suporte à autenticação Digest foi introduzido no Microsoft Internet Explorer 5. |
| NTLM (NT LAN Manager)                     | desafio-resposta | Winsspi.dll          | Um esquema de desafio/resposta que baseia o desafio no nome de usuário.                                                                                                                                                                                                                                                                             |
| Rede da Microsoft (MSN)                   | desafio-resposta | Msnsspc.dll          | O esquema de autenticação da rede da Microsoft.                                                                                                                                                                                                                                                                                                     |
| DPA (autenticação de senha distribuída) | desafio-resposta | Msapsspc.dll         | Semelhante à autenticação do MSN e também é usado pela rede da Microsoft.                                                                                                                                                                                                                                                                           |
| Autenticação de senha remota (RPA)    | CompuServe         | Rpawinet.dll, da.dll | Esquema de autenticação do CompuServe. Para obter mais informações, consulte as [especificações do mecanismo do RPA](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Para qualquer coisa que não seja a autenticação básica, as chaves do registro devem ser configuradas, além da instalação da DLL apropriada.

Se a autenticação for necessária, o sinalizador [ \_ \_ manter \_ conexão da Internet](api-flags.md) deve ser usado na chamada para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). O sinalizador \_ \_ para manter \_ a conexão com a Internet é necessário para NTLM e outros tipos de autenticação para manter a conexão ao concluir o processo de autenticação. Se a conexão não for mantida, o processo de autenticação deverá ser reiniciado com o proxy ou o servidor.

As funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) são concluídas com êxito mesmo quando a autenticação é necessária. A diferença é que os dados retornados nos arquivos de cabeçalho e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) receberão uma página HTML informando ao usuário do código de status.

### <a name="registering-authentication-keys"></a>Registrando chaves de autenticação

INTERNET \_ Open \_ Type a \_ preconfig examina os valores de registro **ProxyEnable**, **ProxyServer** e **ProxyOverride**. Esses valores estão localizados em **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

Para esquemas de autenticação diferentes do básico, uma chave deve ser adicionada ao registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Um valor **DWORD** , **flags**, deve ser definido com o valor apropriado. A lista a seguir mostra os valores possíveis para o valor de **flags** .

-   \_ \_ \_ Contexto exclusivo dos sinalizadores \_ de autenticação do plugin \_ por \_ tcpip (valor = 0x01)

    Cada soquete do protocolo TCP/IP (Transmission Control Protocol/Internet Protocol) contém um contexto diferente. Caso contrário, um novo contexto é passado para cada modelo de URL de bloco ou realm.

-   Os \_ sinalizadores de autenticação do plug-in \_ \_ podem \_ manipular a \_ interface do usuário (valor = 0x02)

    Essa DLL pode tratar sua própria entrada do usuário.

-   Os \_ sinalizadores de autenticação do plug-in \_ \_ \_ não podem lidar com \_ \_ passwd (Value = 0x04)

    Essa DLL pode ser capaz de fazer uma autenticação sem solicitar uma senha ao usuário.

-   \_Sinalizadores de autenticação do plug-in \_ \_ sem \_ Realm (valor = 0x08)

    Essa DLL não usa uma cadeia de caracteres de realm http padrão. Todos os dados que parecem ser um realm são dados específicos do esquema.

-   \_Não são \_ necessários sinalizadores de autenticação do plug-in \_ Keep \_ Alive \_ \_ (valor = 0x10)

    Essa DLL não requer uma conexão persistente para sua sequência de desafio/resposta.

Por exemplo, para adicionar a autenticação NTLM, a chave NTLM deve ser adicionada ao **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, o valor da cadeia de caracteres, **DLLFile** e um valor **DWORD** , **flags**, devem ser adicionados. **DLLFile** deve ser definido como Winsspi.dll e os **sinalizadores** devem ser definidos como 0x08.

### <a name="server-authentication"></a>Autenticação do servidor

Quando um servidor recebe uma solicitação que requer autenticação, o servidor retorna uma mensagem de código de status 401. Nessa mensagem, o servidor deve incluir um ou mais cabeçalhos de resposta WWW-Authenticate. Esses cabeçalhos incluem os métodos de autenticação disponíveis para o servidor. O WinINet escolhe o primeiro método que reconhece.

A autenticação básica fornece segurança fraca, a menos que o canal seja primeiro criptografado por link com SSL ou PCT.

A função [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usada para obter os dados de nome de usuário e senha do usuário, ou uma interface do usuário personalizada pode ser projetada para obter os dados.

Uma interface personalizada pode usar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para definir a [ \_ \_ senha da opção de Internet](option-flags.md) e os valores de nome de [ \_ \_ usuário da opção de Internet](option-flags.md) e, em seguida, reenviar a solicitação para o servidor.

### <a name="proxy-authentication"></a>Autenticação de proxy

Quando um cliente tenta usar um proxy que requer autenticação, o proxy Retorna uma mensagem de código de status 407 para o cliente. Nessa mensagem, o proxy deve incluir um ou mais cabeçalhos de resposta Proxy-Authenticate. Esses cabeçalhos incluem os métodos de autenticação disponíveis do proxy. O WinINet escolhe o primeiro método que reconhece.

A função [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usada para obter os dados de nome de usuário e senha do usuário, ou uma interface do usuário personalizada pode ser projetada.

Uma interface personalizada pode usar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para definir a [ \_ \_ \_ senha do proxy de opção da Internet](option-flags.md) e os valores de nome de [ \_ \_ \_ usuário do proxy de opção de Internet](option-flags.md) e, em seguida, reenviar a solicitação para o proxy.

Se nenhum nome de usuário e senha de proxy forem definidos, o WinINet tentará usar o nome de usuário e a senha para o servidor. Esse comportamento permite que os clientes implementem a mesma interface de usuário personalizada usada para lidar com a autenticação do servidor.

## <a name="handling-http-authentication"></a>Manipulando a autenticação HTTP

A autenticação HTTP pode ser tratada com o [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou com uma função personalizada que usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ou adiciona seus próprios cabeçalhos de autenticação. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode examinar os cabeçalhos associados a um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para localizar erros ocultos, como códigos de status de um proxy ou servidor. O [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pode ser usado para definir o nome de usuário e a senha para o proxy e o servidor. Para a autenticação do MSN e DPA, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) deve ser usado para definir o nome de usuário e a senha.

Para qualquer função personalizada que adicione seus próprios cabeçalhos WWW-Authenticate ou Proxy-Authenticate, o [sinalizador \_ Internet \_ não \_ ](api-flags.md) deve ser definido para desabilitar a autenticação.

O exemplo a seguir mostra como [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usado para manipular a autenticação http.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



No exemplo, dwErrorCode é usado para armazenar quaisquer erros associados à chamada para [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). O [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) é concluído com êxito, mesmo que o proxy ou o servidor exija autenticação. Quando o \_ \_ \_ sinalizador filtro de IU \_ de erro de sinalizadores para \_ erros é passado para [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), a função verifica os cabeçalhos em busca de erros ocultos. Esses erros ocultos incluem qualquer solicitação de autenticação. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) exibe a caixa de diálogo apropriada para solicitar os dados necessários ao usuário. Os sinalizadores da interface do usuário de erros de sinalizadores \_ \_ \_ \_ GERAm \_ dados e sinalizadores sinalizadores de \_ \_ interface do usuário de erro de \_ \_ alteração \_ sinalizadores de opções também devem ser passados para [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), para que a função Construa a estrutura de dados apropriada para o erro e armazene os resultados da caixa de diálogo no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) .

O código de exemplo a seguir mostra como a autenticação pode ser tratada usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 