---
title: HTTP Cookies
description: Cookies HTTP fornecem ao servidor um mecanismo para armazenar e recuperar informações de estado no sistema do aplicativo cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113710"
---
# <a name="http-cookies"></a>HTTP Cookies

Cookies HTTP fornecem ao servidor um mecanismo para armazenar e recuperar informações de estado no sistema do aplicativo cliente. Esse mecanismo permite que aplicativos baseados na Web armazenem informações sobre itens selecionados, preferências do usuário, informações de registro e outras informações que podem ser recuperadas posteriormente.

## <a name="cookie-related-headers"></a>Cookie-Related de Cookie-Related

Há dois headers, Set-Cookie e Cookie, que estão relacionados a cookies. O Set-Cookie é enviado pelo servidor em resposta a uma solicitação HTTP, que é usada para criar um cookie no sistema do usuário. O cabeçalho Cookie é incluído pelo aplicativo cliente com uma solicitação HTTP enviada a um servidor, se houver um cookie que tenha um domínio e caminho correspondentes.

### <a name="set-cookie-header"></a>Set-Cookie de Set-Cookie

O Set-Cookie de resposta usa o seguinte formato:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Uma ou mais sequências de cadeia de caracteres (separadas por ponto e vírgula) que seguem o valor de nome de padrão devem ser incluídas no Set-Cookie  =  de resposta. O servidor pode usar essas sequências de cadeia de caracteres para armazenar dados no sistema do cliente.

A data de validade é definida usando o  formato expire= date , em que *date* é a data de validade em GmT (Hora Média de Greenwich). Se a data de validade não for definida, o cookie expirará após o término da sessão da Internet. Caso contrário, o cookie será persistido no cache até a data de validade. A data deve usar o seguinte formato:

*DAY*, *DD* - *MMM* - *AAAA* *HH:**MM*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*Dia*
</dt> <dd>

O dia da semana (Sun, Mon, Tue, Wed, Thu, Fri, Sat).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*Dd*
</dt> <dd>

O dia do mês (como 01 para o primeiro dia do mês).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*MMM*
</dt> <dd>

A abreviação de três letras do mês (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*Aaaa*
</dt> <dd>

O ano.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*Hh*
</dt> <dd>

O valor de hora no horário do governo (22 seria 22h, por exemplo).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*Mm*
</dt> <dd>

O valor de minuto.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*Ss*
</dt> <dd>

O segundo valor.

</dd> </dl>

Especificar o nome de domínio, usando o domínio padrão= nome de domínio , é opcional para cookies persistentes e é usado para indicar o final do domínio para o qual o cookie é válido.*\_* Cookies de sessão que especificam um domínio são rejeitados. Se o nome de domínio especificado que termina corresponder à solicitação, o cookie tentará corresponder ao caminho para determinar se o cookie deve ser enviado. Por exemplo, se o nome de domínio que termina for .microsoft.com, as solicitações para home.microsoft.com e support.microsoft.com serão verificadas para ver se o padrão especificado corresponde à solicitação. O nome de domínio deve ter pelo menos dois ou três períodos para impedir que os cookies sejam definidos para terminações de nome de domínio amplamente usadas, como .com, .edu e co.jp. Os nomes de domínio que permitem seriam semelhantes a .microsoft.com, .someschool.edu e .someserver.co.jp. Somente hosts dentro do domínio especificado podem definir um cookie para um domínio.

Definir o caminho, usando o caminho padrão= algum caminho, é opcional e pode ser usado para especificar um subconjunto das URLs para as quais o cookie é válido.*\_* Se um caminho for especificado, o cookie será considerado válido para todas as solicitações que corresponderem a esse caminho. Por exemplo, se o caminho especificado for /example, as solicitações com os caminhos /examplecode e /example/code.htm corresponderão. Se nenhum caminho for especificado, presume-se que o caminho seja o caminho do recurso associado ao Set-Cookie de texto.

O cookie também pode ser marcado como seguro, o que especifica que o cookie pode ser enviado somente para servidores https.

Por fim, um cookie pode ser marcado como HttpOnly (os atributos não são sensíveis a minúsculas), para indicar que o cookie não pode ser script e não deve ser revelado para o aplicativo cliente, por motivos de segurança. Dentro Windows Internet, isso significa que o cookie não pode ser recuperado por meio da **função InternetGetCookie.**

### <a name="cookie-header"></a>Cookie Header

O cabeçalho Cookie é incluído em todas as solicitações HTTP que tenham um cookie cujo domínio e caminho corresponderem à solicitação. O header cookie tem o seguinte formato:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Uma ou mais sequências de cadeia de caracteres, usando o valor *de nome de* formato , contêm as informações que foram = definidas no cookie.

## <a name="generating-cookies"></a>Gerando cookies

Há três métodos para gerar cookies para o Microsoft Internet Explorer: usando o Microsoft JScript, usando as funções WinINet e usando um script CGI. Todos os métodos precisam definir as informações incluídas no Set-Cookie de dados.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Gerando um cookie usando o modelo de objeto DHTML

Usando o modelo de objeto HTML dinâmico (DHTML), os cookies podem ser definidos chamando a propriedade **cookie** do objeto de documento, conforme mostrado no exemplo a seguir.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Gerando um cookie usando as funções WinInet

Cookies podem ser criados por aplicativos usando a [**função InternetSetCookie.**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) Para obter mais informações, consulte [Configurando um cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Gerando um cookie usando um script CGI

Os cookies são gerados incluindo um cabeçalho Set-Cookie como parte de um script CGI incluído na resposta HTTP a uma solicitação.

O exemplo a seguir é um script CGI que inclui um Set-Cookie usando Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 