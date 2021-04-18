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
# <a name="http-cookies"></a>Cookies HTTP

Os cookies HTTP fornecem ao servidor um mecanismo para armazenar e recuperar informações de estado no sistema do aplicativo cliente. Esse mecanismo permite aos aplicativos baseados na Web a capacidade de armazenar informações sobre itens selecionados, preferências do usuário, informações de registro e outras informações que podem ser recuperadas posteriormente.

## <a name="cookie-related-headers"></a>Cabeçalhos de Cookie-Related

Há dois cabeçalhos, Set-Cookie e cookie, que estão relacionados a cookies. O cabeçalho de Set-Cookie é enviado pelo servidor em resposta a uma solicitação HTTP, que é usada para criar um cookie no sistema do usuário. O cabeçalho do cookie é incluído pelo aplicativo cliente com uma solicitação HTTP enviada a um servidor, se houver um cookie que tenha um domínio e um caminho correspondentes.

### <a name="set-cookie-header"></a>Cabeçalho de Set-Cookie

O cabeçalho de resposta Set-Cookie usa o seguinte formato:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Uma ou mais sequências de cadeias de caracteres (separadas por ponto e vírgula) que seguem o valor de *nome* de padrão =  devem ser incluídas no cabeçalho de resposta Set-Cookie. O servidor pode usar essas sequências de caracteres para armazenar dados no sistema do cliente.

A data de validade é definida usando o formato Expires =*Date*, em que *Date* é a data de vencimento no GMT (horário de Greenwich). Se a data de expiração não for definida, o cookie expirará após o término da sessão de Internet. Caso contrário, o cookie será persistido no cache até a data de validade. A data deve usar o seguinte formato:

*dia*, *DD* - *Mmm* - *aaaa* *hh*:*mm*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*DIÁRIO*
</dt> <dd>

O dia da semana (sol, segunda-feira, terça-feira, quinta-feira, Sex, Sáb).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*YYYY*
</dt> <dd>

O dia do mês (como 01 para o primeiro dia do mês).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*MMM*
</dt> <dd>

A abreviação de três letras para o mês (Jan, Fev, mar, abr, maio, Jun, Jul, ago, Sep, OCT, Nov, DEC).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*DD*
</dt> <dd>

O ano.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

O valor de hora no tempo militar (22 seria 10:00 P.M., por exemplo).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*MM*
</dt> <dd>

O valor de minuto.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*II*
</dt> <dd>

O segundo valor.

</dd> </dl>

Especificar o nome de domínio, usando o padrão domínio *= \_ nome de domínio*, é opcional para cookies persistentes e é usado para indicar o final do domínio para o qual o cookie é válido. Os cookies de sessão que especificam um domínio são rejeitados. Se o nome de domínio especificado terminar corresponder à solicitação, o cookie tentará corresponder ao caminho para determinar se o cookie deve ser enviado. Por exemplo, se o nome de domínio terminando for. microsoft.com, as solicitações para home.microsoft.com e support.microsoft.com seriam verificadas para ver se o padrão especificado corresponde à solicitação. O nome de domínio deve ter pelo menos dois ou três períodos para impedir que os cookies sejam definidos para terminações de nome de domínio amplamente usadas, como. com,. edu e co.jp. Os nomes de domínio permitidos seriam semelhantes a. microsoft.com,. someschool.edu e. someserver.co.jp. Somente os hosts dentro do domínio especificado podem definir um cookie para um domínio.

A definição do caminho, usando o caminho de padrão =*algum \_ caminho*, é opcional e pode ser usada para especificar um subconjunto das URLs para as quais o cookie é válido. Se um caminho for especificado, o cookie será considerado válido para todas as solicitações que correspondam a esse caminho. Por exemplo, se o caminho especificado for/example, as solicitações com os caminhos/examplecode e/example/code.htm seriam correspondentes. Se nenhum caminho for especificado, o caminho será considerado como o caminho do recurso associado ao cabeçalho de Set-Cookie.

O cookie também pode ser marcado como seguro, o que especifica que o cookie pode ser enviado somente para servidores HTTPS.

Por fim, um cookie pode ser marcado como HttpOnly (os atributos não diferenciam maiúsculas de minúsculas), para indicar que o cookie é não programável e não deve ser revelado ao aplicativo cliente por motivos de segurança. Na Internet do Windows, isso significa que o cookie não pode ser recuperado por meio da função **InternetGetCookie** .

### <a name="cookie-header"></a>Cabeçalho do cookie

O cabeçalho do cookie é incluído em todas as solicitações HTTP que têm um cookie cujo domínio e caminho correspondem à solicitação. O cabeçalho do cookie tem o seguinte formato:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Uma ou mais sequências de cadeias de caracteres, usando o valor de *nome* de formato = , contêm as informações que foram definidas no cookie.

## <a name="generating-cookies"></a>Gerando cookies

Há três métodos para gerar cookies para o Microsoft Internet Explorer: usando o Microsoft JScript, usando as funções do WinINet e usando um script CGI. Todos os métodos precisam definir as informações incluídas no cabeçalho Set-Cookie.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Gerando um cookie usando o modelo de objeto DHTML

Usando o modelo de objeto HTML dinâmico (DHTML), os cookies podem ser definidos chamando a propriedade **Cookie** do objeto Document, conforme mostrado no exemplo a seguir.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Gerando um cookie usando as funções WinInet

Os cookies podem ser criados por aplicativos que usam a função [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) . Para obter mais informações, consulte [Configurando um cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Gerando um cookie usando um script CGI

Os cookies são gerados com a inclusão de um cabeçalho Set-Cookie como parte de um script CGI incluído na resposta HTTP para uma solicitação.

O exemplo a seguir é um script CGI que inclui um cabeçalho Set-Cookie usando o Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 