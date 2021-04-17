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
# <a name="managing-cookies"></a><span data-ttu-id="25577-103">Gerenciando cookies</span><span class="sxs-lookup"><span data-stu-id="25577-103">Managing Cookies</span></span>

<span data-ttu-id="25577-104">No protocolo http, um servidor ou um script usa cookies para manter informações de estado na estação de trabalho cliente.</span><span class="sxs-lookup"><span data-stu-id="25577-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="25577-105">As funções do WinINet implementaram um banco de dados de cookie persistente para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="25577-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="25577-106">Eles podem ser usados para definir cookies no e acessar cookies do banco de dados de cookies.</span><span class="sxs-lookup"><span data-stu-id="25577-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="25577-107">Para obter mais informações, consulte [cookies http](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="25577-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="25577-108">As funções [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) e [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) podem ser usadas para gerenciar cookies.</span><span class="sxs-lookup"><span data-stu-id="25577-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="25577-109">Usando funções de cookie</span><span class="sxs-lookup"><span data-stu-id="25577-109">Using Cookie Functions</span></span>

<span data-ttu-id="25577-110">As funções a seguir permitem que um aplicativo crie ou recupere cookies no banco de dados do cookie.</span><span class="sxs-lookup"><span data-stu-id="25577-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="25577-111">Função</span><span class="sxs-lookup"><span data-stu-id="25577-111">Function</span></span>                                       | <span data-ttu-id="25577-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="25577-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="25577-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="25577-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="25577-114">Recupera cookies para a URL especificada e todas as suas URLs pai.</span><span class="sxs-lookup"><span data-stu-id="25577-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="25577-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="25577-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="25577-116">Define um cookie na URL especificada.</span><span class="sxs-lookup"><span data-stu-id="25577-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="25577-117">Observe que essas funções não exigem uma chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="25577-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="25577-118">Os cookies que têm uma data de expiração são armazenados na conta de usuários locais em usuários \\ "nome de usuário"/ \\ \\ diretório de cookies de roaming do \\ Microsoft \\ Windows \\ e os usuários \\ "username" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies \\ Low Directory for Applications running with low Privileges.</span><span class="sxs-lookup"><span data-stu-id="25577-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="25577-119">Os cookies que não têm uma data de validade são armazenados na memória e estão disponíveis somente para o processo no qual eles foram criados.</span><span class="sxs-lookup"><span data-stu-id="25577-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="25577-120">Conforme observado no tópico [cookies http](http-cookies.md) , a função [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) não retorna cookies que foram marcados pelo servidor como não programáveis com o atributo "HttpOnly" no cabeçalho Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="25577-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="25577-121">Obtendo um cookie</span><span class="sxs-lookup"><span data-stu-id="25577-121">Getting a Cookie</span></span>

<span data-ttu-id="25577-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) retorna os cookies para a URL especificada e todas as suas URLs pai.</span><span class="sxs-lookup"><span data-stu-id="25577-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="25577-123">O exemplo a seguir demonstra uma chamada para [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span><span class="sxs-lookup"><span data-stu-id="25577-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


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



### <a name="setting-a-cookie"></a><span data-ttu-id="25577-124">Configurando um cookie</span><span class="sxs-lookup"><span data-stu-id="25577-124">Setting a Cookie</span></span>

<span data-ttu-id="25577-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) é usado para definir um cookie na URL especificada.</span><span class="sxs-lookup"><span data-stu-id="25577-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="25577-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) pode criar cookies persistentes e de sessão.</span><span class="sxs-lookup"><span data-stu-id="25577-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="25577-127">Os cookies persistentes têm uma data de expiração.</span><span class="sxs-lookup"><span data-stu-id="25577-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="25577-128">Esses cookies são armazenados na conta de usuários locais em usuários \\ "nome de usuário" aplicativos \\ \\ móveis \\ \\ \\ diretório de cookies do Microsoft Windows e os usuários \\ "username" \\ AppData \\ roaming do \\ Microsoft \\ Windows \\ cookies \\ Low Directory for Applications running with low Privileges.</span><span class="sxs-lookup"><span data-stu-id="25577-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="25577-129">Os cookies de sessão são armazenados na memória e podem ser acessados somente pelo processo que os criou.</span><span class="sxs-lookup"><span data-stu-id="25577-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="25577-130">Os dados para o cookie devem estar no formato:</span><span class="sxs-lookup"><span data-stu-id="25577-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="25577-131">Para a data de validade, o formato deve ser:</span><span class="sxs-lookup"><span data-stu-id="25577-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="25577-132">DAY é a abreviação de três letras para o dia da semana, DD é o dia do mês, MMM é a abreviação de três letras para o mês, YYYY é o ano e HH: MM: SS é a hora do dia em hora militar.</span><span class="sxs-lookup"><span data-stu-id="25577-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="25577-133">O exemplo a seguir demonstra duas chamadas para [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span><span class="sxs-lookup"><span data-stu-id="25577-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="25577-134">A primeira chamada cria um cookie de sessão e a segunda cria um cookie persistente.</span><span class="sxs-lookup"><span data-stu-id="25577-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


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
> <span data-ttu-id="25577-135">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="25577-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="25577-136">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="25577-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="25577-137">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="25577-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 