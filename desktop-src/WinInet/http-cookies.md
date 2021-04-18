---
title: Cookies HTTP
description: Os cookies HTTP fornecem ao servidor um mecanismo para armazenar e recuperar informações de estado no sistema do aplicativo cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784539"
---
# <a name="http-cookies"></a><span data-ttu-id="505ee-103">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="505ee-103">HTTP Cookies</span></span>

<span data-ttu-id="505ee-104">Os cookies HTTP fornecem ao servidor um mecanismo para armazenar e recuperar informações de estado no sistema do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="505ee-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="505ee-105">Esse mecanismo permite aos aplicativos baseados na Web a capacidade de armazenar informações sobre itens selecionados, preferências do usuário, informações de registro e outras informações que podem ser recuperadas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="505ee-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="505ee-106">Cabeçalhos de Cookie-Related</span><span class="sxs-lookup"><span data-stu-id="505ee-106">Cookie-Related Headers</span></span>

<span data-ttu-id="505ee-107">Há dois cabeçalhos, Set-Cookie e cookie, que estão relacionados a cookies.</span><span class="sxs-lookup"><span data-stu-id="505ee-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="505ee-108">O cabeçalho de Set-Cookie é enviado pelo servidor em resposta a uma solicitação HTTP, que é usada para criar um cookie no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="505ee-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="505ee-109">O cabeçalho do cookie é incluído pelo aplicativo cliente com uma solicitação HTTP enviada a um servidor, se houver um cookie que tenha um domínio e um caminho correspondentes.</span><span class="sxs-lookup"><span data-stu-id="505ee-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="505ee-110">Cabeçalho de Set-Cookie</span><span class="sxs-lookup"><span data-stu-id="505ee-110">Set-Cookie Header</span></span>

<span data-ttu-id="505ee-111">O cabeçalho de resposta Set-Cookie usa o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="505ee-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="505ee-112">Uma ou mais sequências de cadeias de caracteres (separadas por ponto e vírgula) que seguem o valor de *nome* de padrão =  devem ser incluídas no cabeçalho de resposta Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="505ee-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="505ee-113">O servidor pode usar essas sequências de caracteres para armazenar dados no sistema do cliente.</span><span class="sxs-lookup"><span data-stu-id="505ee-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="505ee-114">A data de validade é definida usando o formato Expires =*Date*, em que *Date* é a data de vencimento no GMT (horário de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="505ee-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="505ee-115">Se a data de expiração não for definida, o cookie expirará após o término da sessão de Internet.</span><span class="sxs-lookup"><span data-stu-id="505ee-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="505ee-116">Caso contrário, o cookie será persistido no cache até a data de validade.</span><span class="sxs-lookup"><span data-stu-id="505ee-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="505ee-117">A data deve usar o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="505ee-117">The date must use the following format:</span></span>

<span data-ttu-id="505ee-118">*dia*, *DD* - *Mmm* - *aaaa* *hh*:*mm*:*SS* GMT</span><span class="sxs-lookup"><span data-stu-id="505ee-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="505ee-119"><span id="DAY"></span><span id="day"></span>*DIÁRIO*</span><span class="sxs-lookup"><span data-stu-id="505ee-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-120">O dia da semana (sol, segunda-feira, terça-feira, quinta-feira, Sex, Sáb).</span><span class="sxs-lookup"><span data-stu-id="505ee-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="505ee-121"><span id="DD"></span><span id="dd"></span>*YYYY*</span><span class="sxs-lookup"><span data-stu-id="505ee-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-122">O dia do mês (como 01 para o primeiro dia do mês).</span><span class="sxs-lookup"><span data-stu-id="505ee-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="505ee-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span><span class="sxs-lookup"><span data-stu-id="505ee-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-124">A abreviação de três letras para o mês (Jan, Fev, mar, abr, maio, Jun, Jul, ago, Sep, OCT, Nov, DEC).</span><span class="sxs-lookup"><span data-stu-id="505ee-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="505ee-125"><span id="YYYY"></span><span id="yyyy"></span>*DD*</span><span class="sxs-lookup"><span data-stu-id="505ee-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-126">O ano.</span><span class="sxs-lookup"><span data-stu-id="505ee-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="505ee-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="505ee-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-128">O valor de hora no tempo militar (22 seria 10:00 P.M., por exemplo).</span><span class="sxs-lookup"><span data-stu-id="505ee-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="505ee-129"><span id="MM"></span><span id="mm"></span>*MM*</span><span class="sxs-lookup"><span data-stu-id="505ee-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-130">O valor de minuto.</span><span class="sxs-lookup"><span data-stu-id="505ee-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="505ee-131"><span id="SS"></span><span id="ss"></span>*II*</span><span class="sxs-lookup"><span data-stu-id="505ee-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="505ee-132">O segundo valor.</span><span class="sxs-lookup"><span data-stu-id="505ee-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="505ee-133">Especificar o nome de domínio, usando o padrão domínio *= \_ nome de domínio*, é opcional para cookies persistentes e é usado para indicar o final do domínio para o qual o cookie é válido.</span><span class="sxs-lookup"><span data-stu-id="505ee-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="505ee-134">Os cookies de sessão que especificam um domínio são rejeitados.</span><span class="sxs-lookup"><span data-stu-id="505ee-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="505ee-135">Se o nome de domínio especificado terminar corresponder à solicitação, o cookie tentará corresponder ao caminho para determinar se o cookie deve ser enviado.</span><span class="sxs-lookup"><span data-stu-id="505ee-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="505ee-136">Por exemplo, se o nome de domínio terminando for. microsoft.com, as solicitações para home.microsoft.com e support.microsoft.com seriam verificadas para ver se o padrão especificado corresponde à solicitação.</span><span class="sxs-lookup"><span data-stu-id="505ee-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="505ee-137">O nome de domínio deve ter pelo menos dois ou três períodos para impedir que os cookies sejam definidos para terminações de nome de domínio amplamente usadas, como. com,. edu e co.jp.</span><span class="sxs-lookup"><span data-stu-id="505ee-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="505ee-138">Os nomes de domínio permitidos seriam semelhantes a. microsoft.com,. someschool.edu e. someserver.co.jp.</span><span class="sxs-lookup"><span data-stu-id="505ee-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="505ee-139">Somente os hosts dentro do domínio especificado podem definir um cookie para um domínio.</span><span class="sxs-lookup"><span data-stu-id="505ee-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="505ee-140">A definição do caminho, usando o caminho de padrão =*algum \_ caminho*, é opcional e pode ser usada para especificar um subconjunto das URLs para as quais o cookie é válido.</span><span class="sxs-lookup"><span data-stu-id="505ee-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="505ee-141">Se um caminho for especificado, o cookie será considerado válido para todas as solicitações que correspondam a esse caminho.</span><span class="sxs-lookup"><span data-stu-id="505ee-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="505ee-142">Por exemplo, se o caminho especificado for/example, as solicitações com os caminhos/examplecode e/example/code.htm seriam correspondentes.</span><span class="sxs-lookup"><span data-stu-id="505ee-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="505ee-143">Se nenhum caminho for especificado, o caminho será considerado como o caminho do recurso associado ao cabeçalho de Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="505ee-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="505ee-144">O cookie também pode ser marcado como seguro, o que especifica que o cookie pode ser enviado somente para servidores HTTPS.</span><span class="sxs-lookup"><span data-stu-id="505ee-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="505ee-145">Por fim, um cookie pode ser marcado como HttpOnly (os atributos não diferenciam maiúsculas de minúsculas), para indicar que o cookie é não programável e não deve ser revelado ao aplicativo cliente por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="505ee-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="505ee-146">Na Internet do Windows, isso significa que o cookie não pode ser recuperado por meio da função **InternetGetCookie** .</span><span class="sxs-lookup"><span data-stu-id="505ee-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="505ee-147">Cabeçalho do cookie</span><span class="sxs-lookup"><span data-stu-id="505ee-147">Cookie Header</span></span>

<span data-ttu-id="505ee-148">O cabeçalho do cookie é incluído em todas as solicitações HTTP que têm um cookie cujo domínio e caminho correspondem à solicitação.</span><span class="sxs-lookup"><span data-stu-id="505ee-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="505ee-149">O cabeçalho do cookie tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="505ee-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="505ee-150">Uma ou mais sequências de cadeias de caracteres, usando o valor de *nome* de formato = , contêm as informações que foram definidas no cookie.</span><span class="sxs-lookup"><span data-stu-id="505ee-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="505ee-151">Gerando cookies</span><span class="sxs-lookup"><span data-stu-id="505ee-151">Generating Cookies</span></span>

<span data-ttu-id="505ee-152">Há três métodos para gerar cookies para o Microsoft Internet Explorer: usando o Microsoft JScript, usando as funções do WinINet e usando um script CGI.</span><span class="sxs-lookup"><span data-stu-id="505ee-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="505ee-153">Todos os métodos precisam definir as informações incluídas no cabeçalho Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="505ee-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="505ee-154">Gerando um cookie usando o modelo de objeto DHTML</span><span class="sxs-lookup"><span data-stu-id="505ee-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="505ee-155">Usando o modelo de objeto HTML dinâmico (DHTML), os cookies podem ser definidos chamando a propriedade **Cookie** do objeto Document, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="505ee-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="505ee-156">Gerando um cookie usando as funções WinInet</span><span class="sxs-lookup"><span data-stu-id="505ee-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="505ee-157">Os cookies podem ser criados por aplicativos que usam a função [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="505ee-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="505ee-158">Para obter mais informações, consulte [Configurando um cookie](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="505ee-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="505ee-159">Gerando um cookie usando um script CGI</span><span class="sxs-lookup"><span data-stu-id="505ee-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="505ee-160">Os cookies são gerados com a inclusão de um cabeçalho Set-Cookie como parte de um script CGI incluído na resposta HTTP para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="505ee-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="505ee-161">O exemplo a seguir é um script CGI que inclui um cabeçalho Set-Cookie usando o Perl.</span><span class="sxs-lookup"><span data-stu-id="505ee-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="505ee-162">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="505ee-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="505ee-163">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="505ee-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="505ee-164">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="505ee-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 