---
title: Configurando e recuperando opções da Internet
description: Este tópico descreve como definir e recuperar opções da Internet usando as funções InternetSetOption e InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Configurando e recuperando opções da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823922"
---
# <a name="setting-and-retrieving-internet-options"></a>Configurando e recuperando opções da Internet

Este tópico descreve como definir e recuperar opções da Internet usando as funções [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .

As opções da Internet podem ser definidas em ou recuperadas de um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado ou as configurações atuais no Microsoft Internet Explorer.

-   [Etapas de implementação](#implementation-steps)
    -   [Escolhendo Opções da Internet](#choosing-internet-options)
    -   [Escolhendo o identificador HINTERNET](#choosing-the-hinternet-handle)
    -   [Configurando ou recuperando as opções](#setting-or-retrieving-the-options)
-   [Escopo do identificador de HINTERNET](#scope-of-hinternet-handle)
-   [Definindo opções individuais](#setting-individual-options)
-   [Recuperando opções individuais](#retrieving-individual-options)
    -   [Exemplo completo](#complete-sample)
-   [Definindo opções de conexão](#setting-connection-options)
-   [Recuperando opções de conexão](#retrieving-connection-options)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-steps"></a>Etapas de implementação

Para definir ou recuperar as opções da Internet, conclua o seguinte:

-   [Escolhendo Opções da Internet](#choosing-internet-options)
-   [Escolhendo o identificador HINTERNET](#choosing-the-hinternet-handle)
-   [Configurando ou recuperando as opções](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Escolhendo Opções da Internet

Como há tantas opções da Internet, a escolha das opções corretas é importante. Muitas opções da Internet afetam o comportamento das funções WinINet e do Internet Explorer:

Por exemplo, você pode:

-   Manipule a autenticação básica de servidor e proxy definindo nomes de usuário e senhas.
-   Defina ou recupere a cadeia de caracteres do agente do usuário usada pelos servidores para identificar os recursos do aplicativo cliente ou do navegador.
-   Recupere o tipo de identificador do identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.

Para obter mais informações e uma lista das opções da Internet, consulte [**sinalizadores de opção**](option-flags.md).

No Internet Explorer 5 e posterior, algumas opções podem ser definidas ou recuperadas de uma conexão de Internet específica usando a lista de opções [**Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) e as estruturas de [**opção de Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) . Para obter mais informações e uma lista de opções que podem ser definidas ou recuperadas de uma conexão de Internet específica, consulte o membro **dwOptions** da estrutura da [**\_ opção Internet por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .

### <a name="choosing-the-hinternet-handle"></a>Escolhendo o identificador HINTERNET

O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) usado para definir ou recuperar as opções da Internet determina o escopo da operação. Todos os identificadores criados por meio desse identificador herdarão as opções definidas nesse identificador.

Por exemplo, aplicativos cliente que exigem um proxy com autenticação, provavelmente não exigem a configuração do nome de usuário e da senha do proxy sempre que o aplicativo tentar acessar um recurso da Internet. Se todas as solicitações em uma determinada conexão forem tratadas pelo mesmo proxy, definir o nome de usuário e a senha do proxy em um tipo de conexão [**HINTERNET**](appendix-a-hinternet-handles.md) identificador, ou seja, um identificador criado por uma chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permitiria que qualquer chamada derivada desse identificador **HINTERNET** use o mesmo nome de usuário e senha do proxy. Definir o nome de usuário e a senha do proxy sempre que um identificador de **HINTERNET** é criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) exigiria sobrecarga extra e desnecessária. Lembre-se de que, se o aplicativo usar um proxy que requer autenticação, ele deverá definir as credenciais de proxy em cada nova conexão.

### <a name="setting-or-retrieving-the-options"></a>Configurando ou recuperando as opções

Quando você tiver determinado o que as opções da Internet e o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para usar, recupere essas opções da Internet. Para definir ou recuperar opções, chame [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Escopo do identificador de HINTERNET

O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) usado para definir ou recuperar as opções da Internet determina as ações para as quais as opções são válidas.

Esses identificadores têm três níveis:

-   O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raiz (criado por uma chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) conterá todas as opções da Internet que afetam essa instância do Wininet.
-   [**HINTERNET**](appendix-a-hinternet-handles.md) identificadores que se conectam a um servidor (criado por uma chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))
-   Identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) associados a um recurso ou enumeração de recursos em um servidor específico.

Além dos vários identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , um aplicativo também pode usar **NULL** para definir ou recuperar os valores padrão das opções da Internet usadas pelo Internet Explorer e as funções do Wininet. Definir opções da Internet ao usar **NULL** como o identificador altera os valores padrão das opções, que atualmente estão armazenadas no registro. Os aplicativos cliente não devem usar funções de registro para alterar os valores padrão das opções da Internet, pois a implementação de como as opções são armazenadas pode ser alterada no futuro.

A tabela a seguir lista o tipo de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) e o escopo das opções da Internet associadas a eles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de identificador</th>
<th>Escopo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>As configurações de opção padrão para o Internet Explorer.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>As configurações de opção para essa conexão com um servidor FTP. Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>As configurações de opção para essa conexão com um servidor gopher. Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>As configurações de opção para essa conexão com um servidor HTTP. Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>As configurações de opção associadas a essa solicitação de arquivo.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>As configurações de opção associadas a este download de recurso de FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>As configurações de opção associadas a este download de recurso de FTP são formatadas em HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>As configurações de opção associadas a esta pesquisa de arquivos em um servidor FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>As configurações de opção associadas a esta pesquisa de arquivos em um servidor FTP formatado em HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>As configurações de opção associadas a este download de recurso do Gopher.
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>As configurações de opção associadas a este download de recurso do Gopher são formatadas em HTML.
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>As configurações de opção associadas a esta pesquisa de arquivos em um servidor gopher.
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>As configurações de opção associadas a esta pesquisa de arquivos em um servidor gopher formatado em HTML.
<blockquote>
[!Note]<br />
Somente Windows XP e Windows Server 2003 R2 e versões anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>As configurações de opção associadas a essa solicitação HTTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>As configurações de opção associadas a esta instância das funções WinINet.</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>Definindo opções individuais

Depois de determinar as opções da Internet que você deseja definir e o escopo que você deseja que sejam afetados por essas opções, a definição de opções da Internet não é complicada. Tudo o que você precisa fazer é chamar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) desejado, o sinalizador de opção da Internet e um buffer que contém as informações que você deseja definir.

O exemplo a seguir mostra como definir o nome de usuário e a senha do proxy em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Recuperando opções individuais

As opções da Internet podem ser recuperadas usando a função [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) . Para recuperar as opções da Internet:

1.  Determine o tamanho do buffer necessário para recuperar as informações da opção da Internet.

    O tamanho do buffer pode ser determinado usando **NULL** para o endereço do buffer e passando um tamanho de buffer igual a zero.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    O valor retornado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) é a quantidade de memória necessária para recuperar as informações, em bytes.

2.  Aloque uma memória para o buffer.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Recupere os dados.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Libere a memória.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Exemplo completo

Veja a seguir o exemplo completo usado na seção anterior. Este exemplo mostra como recuperar a cadeia de caracteres do agente do usuário padrão.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Definindo opções de conexão

No Internet Explorer 5 e posterior, as opções da Internet podem ser definidas para em uma conexão específica. Anteriormente, todas as conexões compartilharam as mesmas configurações de opção de Internet. Para definir opções para uma conexão específica:

1.  Crie uma estrutura de [**lista de opções de Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Aloque a memória para as opções individuais da Internet que você deseja definir para a conexão.
3.  Defina as opções em estruturas de [**opção de Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Defina as opções usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

O exemplo de código a seguir mostra como definir dados de proxy para uma conexão de LAN.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Recuperando opções de conexão

No Internet Explorer 5 e posterior, as opções da Internet podem ser recuperadas de uma conexão específica. Para recuperar opções de uma conexão específica:

1.  Crie uma estrutura de [**lista de opções de Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Aloque a memória para as opções individuais da Internet a serem recuperadas da conexão.
3.  Especifique as opções usando as estruturas de [**opção da Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Recupere as opções usando [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Utilize os dados da opção.
6.  Libere a memória, alocada para conter os dados da opção, usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando a autenticação](handling-authentication.md)
</dt> <dt>

[Identificadores de HINTERNET](appendix-a-hinternet-handles.md)
</dt> </dl>

 

