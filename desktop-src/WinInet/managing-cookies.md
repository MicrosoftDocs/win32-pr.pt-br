---
title: Gerenciando cookies
description: No protocolo http, um servidor ou um script usa cookies para manter informações de estado na estação de trabalho cliente.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105748351"
---
# <a name="managing-cookies"></a>Gerenciando cookies

No protocolo http, um servidor ou um script usa cookies para manter informações de estado na estação de trabalho cliente. As funções do WinINet implementaram um banco de dados de cookie persistente para essa finalidade. Eles podem ser usados para definir cookies no e acessar cookies do banco de dados de cookies. Para obter mais informações, consulte [cookies http](http-cookies.md).

As funções [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) e [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) podem ser usadas para gerenciar cookies.

## <a name="using-cookie-functions"></a>Usando funções de cookie

As funções a seguir permitem que um aplicativo crie ou recupere cookies no banco de dados do cookie.



| Função                                       | Descrição                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Recupera cookies para a URL especificada e todas as suas URLs pai. |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Define um cookie na URL especificada.                              |



 

Observe que essas funções não exigem uma chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Os cookies que têm uma data de expiração são armazenados na conta de usuários locais em usuários \\ "nome de usuário"/ \\ \\ diretório de cookies de roaming do \\ Microsoft \\ Windows \\ e os usuários \\ "username" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies \\ Low Directory for Applications running with low Privileges. Os cookies que não têm uma data de validade são armazenados na memória e estão disponíveis somente para o processo no qual eles foram criados.

Conforme observado no tópico [cookies http](http-cookies.md) , a função [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) não retorna cookies que foram marcados pelo servidor como não programáveis com o atributo "HttpOnly" no cabeçalho Set-Cookie.

### <a name="getting-a-cookie"></a>Obtendo um cookie

[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) retorna os cookies para a URL especificada e todas as suas URLs pai.

O exemplo a seguir demonstra uma chamada para [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a>Configurando um cookie

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) é usado para definir um cookie na URL especificada. [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) pode criar cookies persistentes e de sessão.

Os cookies persistentes têm uma data de expiração. Esses cookies são armazenados na conta de usuários locais em usuários \\ "nome de usuário" aplicativos \\ \\ móveis \\ \\ \\ diretório de cookies do Microsoft Windows e os usuários \\ "username" \\ AppData \\ roaming do \\ Microsoft \\ Windows \\ cookies \\ Low Directory for Applications running with low Privileges.

Os cookies de sessão são armazenados na memória e podem ser acessados somente pelo processo que os criou.

Os dados para o cookie devem estar no formato:

``` syntax
NAME=VALUE
```

Para a data de validade, o formato deve ser:

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

DAY é a abreviação de três letras para o dia da semana, DD é o dia do mês, MMM é a abreviação de três letras para o mês, YYYY é o ano e HH: MM: SS é a hora do dia em hora militar.

O exemplo a seguir demonstra duas chamadas para [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea). A primeira chamada cria um cookie de sessão e a segunda cria um cookie persistente.


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 