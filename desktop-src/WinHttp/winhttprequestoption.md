---
description: inclui opções que podem ser definidas ou recuperadas para a sessão atual do WinHTTP (Microsoft Windows HTTP Services).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Enumeração WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051874"
---
# <a name="winhttprequestoption-enumeration"></a>Enumeração WinHttpRequestOption

a enumeração **WinHttpRequestOption** inclui opções que podem ser definidas ou recuperadas para a sessão atual do WinHTTP (Microsoft Windows HTTP Services).

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Useragentstring do WinHttpRequestOption \_**
</dt> <dd>

Define ou recupera uma **variante** que contém a cadeia de caracteres do [*agente do usuário*](glossary.md) .

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**URL do WinHttpRequestOption \_**
</dt> <dd>

Recupera uma **variante** que contém a URL do recurso. Esse valor é somente leitura; Você não pode definir a URL usando essa propriedade. A URL não pode ser lida até que o método [**Open**](iwinhttprequest-open.md) seja chamado. Essa opção é útil para verificar a URL depois que o método [**Send**](iwinhttprequest-send.md) for concluído para verificar se ocorreu algum redirecionamento.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

Define ou recupera uma **variante** que identifica a [*página de código*](glossary.md) da cadeia de caracteres da URL. O valor padrão é a página de código UTF-8. A página de código é usada para converter a cadeia de caracteres da URL Unicode, passada no método [**Open**](iwinhttprequest-open.md) , para uma representação de cadeia de caracteres de byte único.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Define ou recupera uma **variante** que indica se os caracteres percentuais na cadeia de caracteres da URL são convertidos em uma sequência de escape. O valor padrão dessa opção é **Variant \_ true** , que especifica todos os caracteres de American National Standards Institute não seguros (ANSI), exceto que o símbolo de porcentagem é convertido em uma sequência de escape.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Define ou recupera uma **variante** que indica quais erros de certificado de servidor devem ser ignorados. Isso pode ser uma combinação de um ou mais dos sinalizadores a seguir.



| Erro                                                  | Valor  |
|--------------------------------------------------------|--------|
| Autoridade de certificação (CA) desconhecida ou raiz não confiável | 0x0100 |
| Uso incorreto                                            | 0x0200 |
| Nome comum inválido (CN)                               | 0x1000 |
| Data inválida ou certificado expirado                    | 0x2000 |



 

O valor padrão dessa opção na versão 5,1 do WinHTTP é zero, o que resulta em nenhum erro ignorado. Em versões anteriores do WinHTTP, a configuração padrão era 0x3300, o que resultou em todos os erros de certificado do servidor sendo ignorados por padrão.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Define uma **variante** que especifica o certificado do cliente que é enviado a um servidor para autenticação. Essa opção indica o local, o [*repositório de certificados*](glossary.md)e o assunto de um certificado de cliente delimitado por barras invertidas. Para obter mais informações sobre como selecionar um certificado de cliente, consulte [SSL no WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Define ou recupera uma **variante** que indica se as solicitações são redirecionadas automaticamente quando o servidor especifica um novo local para o recurso. O valor padrão dessa opção é **Variant \_ true** para indicar que as solicitações são redirecionadas automaticamente.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

Define ou recupera uma **variante** que indica se caracteres não seguros no caminho e os componentes de consulta de uma URL são convertidos em sequências de escape. O valor padrão dessa opção é **Variant \_ true**, que especifica que os caracteres no caminho e na consulta são convertidos.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Define ou recupera uma **variante** que indica se caracteres não seguros no componente de consulta da URL são convertidos em sequências de escape. O valor padrão dessa opção é **Variant \_ true**, que especifica que os caracteres na consulta são convertidos.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Define ou recupera uma **variante** que indica quais protocolos seguros podem ser usados. Essa opção seleciona os protocolos aceitáveis para o cliente. O protocolo é negociado durante o handshake de protocolo SSL (SSL). Isso pode ser uma combinação de um ou mais dos sinalizadores a seguir.



| Protocolo                           | Valor  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Segurança de camada de transporte (TLS) 1,0 | 0x0080 |



 

O valor padrão dessa opção é 0x0028, que indica que o SSL 2,0 ou SSL 3,0 pode ser usado. Se essa opção for definida como zero, o cliente e o servidor não poderão determinar um protocolo de segurança aceitável e o próximo [**envio**](iwinhttprequest-send.md) resultará em um erro.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**
</dt> <dd>

Define ou recupera uma **variante** que indica se o rastreamento está habilitado no momento. para obter mais informações sobre o recurso de rastreamento no Microsoft Windows serviços HTTP (WinHTTP), consulte [recursos de rastreamento do winhttp](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Controla se o objeto [**WinHttpRequest**](winhttprequest.md) reverte temporariamente a representação do cliente pela duração das operações de autenticação do certificado SSL. A configuração padrão para o objeto **WinHttpRequest** é **true**. Defina essa opção como **false** para manter a representação ao executar operações de autenticação de certificado.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Controla se o WinHTTP permite ou não redirecionamentos. Por padrão, todos os redirecionamentos são automaticamente seguidos, exceto aqueles que são transferidos de uma URL segura (https) para uma URL não segura (http). Defina essa opção como **true** para habilitar HTTPS para redirecionamentos http.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Habilita ou desabilita o suporte para autenticação do Passport. Por padrão, o suporte automático para autenticação do Passport está desabilitado; Defina essa opção como **true** para habilitar o suporte à autenticação do Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Define ou recupera o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10. Esse limite impede que sites não autorizados tornem a parada do cliente WinHTTP após um grande número de redirecionamentos.

**Windows XP com SP1 e Windows 2000 com SP3:** Não há suporte para esse valor de enumeração.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Define ou recupera um conjunto associado no tamanho máximo da parte do cabeçalho da resposta do servidor. Essa ligação protege o cliente de um servidor mal-intencionado tentando paralisar o cliente enviando uma resposta com uma quantidade infinita de dados de cabeçalho. O valor padrão é 64 KB.

**Windows XP com SP1 e Windows 2000 com SP3:** Não há suporte para esse valor de enumeração.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Define ou recupera um limite na quantidade de dados que será descarregada de respostas para reutilizar uma conexão. O padrão é 1 MB.

**Windows XP com SP1 e Windows 2000 com SP3:** Não há suporte para esse valor de enumeração.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Define ou recupera um valor booliano que indica se HTTP/1.1 ou HTTP/1.0 devem ser usados. O padrão é **true**, para que http/1.1 seja usado por padrão.

**Windows XP com SP1 e Windows 2000 com SP3:** Não há suporte para esse valor de enumeração.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Habilita a verificação de revogação de certificado do servidor durante a negociação SSL. Quando o servidor apresenta um certificado, uma verificação é executada para determinar se o certificado foi revogado pelo emissor. Se o certificado for realmente revogado ou a verificação de revogação falhar porque a CRL (lista de certificados revogados) não pode ser baixada, a solicitação falhará; esses erros de revogação não podem ser suprimidos.

**Windows XP com SP1 e Windows 2000 com SP3:** Não há suporte para esse valor de enumeração.

</dd> </dl>

## <a name="remarks"></a>Comentários

De definir uma opção especificando uma das constantes anteriores como o parâmetro da [**propriedade Option.**](iwinhttprequest-option.md)

> [!Note]  
> Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




