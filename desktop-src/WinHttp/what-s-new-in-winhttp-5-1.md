---
description: Este tópico descreve as diferenças mais importantes entre o WinHTTP versão 5,1 e a versão 5,0.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Novidades no WinHTTP 5,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909d5ae8fb1d169af01782d21d2ead56b25c940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812357"
---
# <a name="whats-new-in-winhttp-51"></a>O que há de novo no WinHTTP 5,1

Este tópico descreve as diferenças mais importantes entre o WinHTTP versão 5,1 e a versão 5,0. Muitas dessas diferenças exigem alterações de código em aplicativos que migram da versão 5,0 para a versão 5,1. Alguns dos recursos da versão 5,1 estão disponíveis apenas a partir do Windows Server 2003 e do Windows XP com Service Pack 2 (SP2), particularmente os recursos relacionados ao aprimoramento da segurança do cliente em servidores Web mal-intencionados.

> [!IMPORTANT]
> Com o lançamento do WinHTTP versão 5,1, o download do WinHTTP 5,0 não está mais disponível. A partir de 1º de outubro de 2004, a Microsoft removeu o download do SDK do WinHTTP 5,0 do MSDN e terminou o suporte do produto para a versão 5,0.

 

## <a name="dll-name-change"></a>Alteração de nome de DLL

O nome da nova DLL do WinHTTP 5,1 é Winhttp.dll, enquanto o nome da DLL do WinHTTP 5,0 é Winhttp5.dll.

O WinHTTP 5,0 e o 5,1 podem coexistir no mesmo sistema; O WinHTTP 5,1 não substitui, nem instala, o WinHTTP 5,0.

## <a name="redistribution"></a>Redistribuição

O WinHTTP 5,1 está disponível apenas com o Windows Server 2003, Windows 2000 Professional com Service Pack 3 (SP3), Windows XP com Service Pack 1 (SP1) e sistemas operacionais posteriores. Um arquivo de módulo de mesclagem redistribuível (. msm) não está disponível para o WinHTTP 5,1.

## <a name="winhttprequest-progid"></a>ProgID de WinHttpRequest

O ProgID do componente WinHttpRequest mudou de "WinHttp. WinHttpRequest. 5" para "WinHttp. WinHttpRequest. 5.1". O CLSID da classe [**WinHttpRequest**](winhttprequest.md) também foi alterado.

## <a name="async-callback-behavior-change"></a>Alteração de comportamento de retorno de chamada assíncrono

Ao chamar as funções [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) e [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) no modo assíncrono, não dependa dos respectivos parâmetros *lpdwNumberOfBytesWritten*, *lpdwNumberOfBytesAvailable* e *lpdwNumberOfBytesRead* out a serem definidos. Se a chamada de função for concluída de forma assíncrona, o WinHTTP não gravará nesses ponteiros fornecidos pelo código do aplicativo. Em vez disso, o aplicativo deve recuperar esses valores usando parâmetros *lpvStatusInformation* e *dwStatusInformationLength* para a função de retorno de chamada.

## <a name="changes-to-default-settings"></a>Alterações nas configurações padrão

As alterações nas configurações padrão incluem:

-   A verificação de certificado do servidor SSL está habilitada por padrão no WinHTTP 5,1. O WinHTTP 5,0 não trata as falhas encontradas ao validar o certificado do servidor como erros fatais; Eles são relatados ao aplicativo usando uma notificação de retorno de chamada de **\_ falha segura** , mas não fazem com que a solicitação seja anulada. O WinHTTP 5,1, como alternativa, trata falhas de validação de certificado do servidor como erros fatais que anulam a solicitação. O aplicativo pode instruir o WinHTTP a ignorar um pequeno subconjunto de erros de certificado, como autoridade de certificação desconhecida, data de certificado inválida/expirada ou nome de entidade de certificado inválido, usando a opção de **\_ sinalizadores de \_ segurança \_ de opção WinHTTP** .
-   O suporte à autenticação do Passport está desabilitado por padrão no WinHTTP 5,1. O suporte do Passport pode ser habilitado com a **opção WinHTTP configurar a opção \_ \_ \_ Passport \_ auth** . A pesquisa automática de credenciais do Passport no keyring também é desabilitada por padrão.
-   Redirecionar alteração de comportamento: redirecionamentos de HTTP de um **https seguro:** a URL para um **http:** a URL regular não é mais seguida automaticamente por padrão por motivos de segurança. Há uma nova opção, a **\_ \_ \_ política de redirecionamento de opção WinHTTP**, para substituir o comportamento de redirecionamento padrão no WinHTTP 5,1. Com o componente com **WinHttpRequest** , use a nova opção **WinHttpRequestOption \_ EnableHttpsToHttpRedirects** para habilitar redirecionamentos de https: para http: URLs.
-   Quando um arquivo de rastreamento WinHTTP é criado, o acesso é restrito a uma ACL, de modo que somente os administradores possam ler ou gravar o arquivo. A conta de usuário sob a qual o TraceFile foi criado também pode modificar a ACL para conceder a outros acessos. Essa proteção está disponível somente em sistemas de arquivos que dão suporte à segurança; ou seja, NTFS, não FAT32).
-   A partir do Windows Server 2003 e do Windows XP com SP2, o envio de solicitações para as seguintes portas não-HTTP conhecidas é restrito por motivos de segurança: 21 (FTP), 25 (SMTP), 70 (GOPHER), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   A partir do Windows Server 2003 e do Windows XP com SP2, a quantidade máxima de dados de cabeçalho que o WinHTTP aceita em uma resposta HTTP é de 64K, por padrão. Se a resposta HTTP do servidor contiver mais de 64K de dados de cabeçalho totais, WinHTTP falhará na solicitação com um erro WinHTTP erro de **\_ \_ \_ \_ resposta do servidor inválido** . Esse limite de 64K pode ser substituído usando a opção nova **opção de tamanho do \_ cabeçalho de \_ \_ resposta de \_ \_ máximo de WinHTTP** .

## <a name="ipv6-support"></a>Suporte a IPv6

O WinHTTP 5,1 adiciona suporte para o protocolo IP versão 6 (IPv6). O WinHTTP pode enviar solicitações HTTP para um servidor cujo nome DNS seja resolvido em um endereço IPv6 e, a partir do Windows Server 2003 e do Windows XP com SP2, o WinHTTP também oferece suporte a endereços IPv6 literais.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Novas opções na API C/C++ para WinHTTP

O WinHTTP 5,1 implementa as seguintes novas opções:

<dl> " \# definir a \_ opção WinHTTP \_ sair do Passport \_ \_ 86"  
" \# definir a \_ opção WinHTTP \_ URL de retorno do Passport \_ \_ 87"  
" \# definir a \_ \_ política de redirecionamento de opção WinHTTP \_ 88"  
</dl>

A partir do Windows Server 2003 e do Windows XP com SP2, o WinHTTP 5,1 implementa as novas opções a seguir. No Windows 2000 Professional com SP3 ou Windows XP com SP1, no entanto, as chamadas para [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ou [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com essas IDs de opção falham:

<dl> " \# definir a \_ opção de WinHTTP \_ \_ tempo limite de resposta de recebimento \_ 7"  
" \# definir a \_ opção WinHTTP máx. de \_ \_ \_ redirecionamentos automáticos de http \_ 89"  
" \# definir o \_ \_ status http máximo da opção WinHTTP \_ \_ \_ continuar 90"  
" \# definir o \_ tamanho do cabeçalho de resposta máximo da opção de WinHTTP \_ \_ \_ \_ 91"  
" \# definir o \_ tamanho de dreno de resposta máximo da opção de WinHTTP \_ \_ \_ \_ 92"  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Novas opções no componente WinHttpRequest 5,1

O componente WinHttpRequest 5,1 implementa as seguintes novas opções:

<dl> "WinHttpRequestOption \_ RevertImpersonationOverSsl"  
"WinHttpRequestOption \_ EnableHttpsToHttpRedirects"  
"WinHttpRequestOption \_ EnablePassportAuthentication"  
</dl>

As seguintes novas opções WinHttpRequest 5,1 estão disponíveis a partir do Windows Server 2003 e do Windows XP com SP2:

<dl> "WinHttpRequestOption \_ MaxAutomaticRedirects"  
"WinHttpRequestOption \_ MaxResponseHeaderSize"  
"WinHttpRequestOption \_ MaxResponseDrainSize"  
"WinHttpRequestOptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>Os proxies não são confiáveis quando a segurança de logon automático está definida como alta

No WinHTTP 5,0, os servidores proxy são sempre confiáveis para logon automático. Isso não é mais válido para o WinHTTP 5,1 em execução no Windows Server 2003 e no Windows XP com SP2 quando a opção de política **alta de nível de segurança do WinHTTP \_ autologonn \_ \_ \_** estiver definida.

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API de descoberta automática de proxy da Web (AutoProxy)

Para facilitar a configuração de configurações de proxy para aplicativos baseados em WinHTTP, o WinHTTP agora implementa o protocolo WPAD (descoberta automática de proxy da Web), também conhecido como *AutoProxy*. Esse é o mesmo protocolo que os navegadores da Web, como o Internet Explorer, implementam para descobrir a configuração de proxy automaticamente sem exigir que um usuário final especifique um servidor proxy manualmente. Para dar suporte ao AutoProxy, o WinHTTP 5,1 implementa uma nova função C/C++, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), além de duas funções de suporte, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Problemas conhecidos

Os problemas a seguir são conhecidos por existir no WinHTTP 5,1 no Windows 2000 Professional com SP3 e no Windows XP com SP1. Esses problemas são resolvidos para o WinHTTP a partir do Windows Server 2003 e do Windows XP com SP2:

-   Se o aplicativo usar a função [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) ou o método [**settempo_limites**](iwinhttprequest-settimeouts.md) no componente [**WinHttpRequest**](iwinhttprequest-interface.md) para definir um tempo limite de resolução de DNS não infinito, como o parâmetro *dwResolveTimeout* , ocorrerá um vazamento de identificador de thread cada vez que o WinHTTP resolver um nome DNS. Em um grande número de solicitações HTTP, isso causa um vazamento significativo na memória. A solução alternativa é deixar a configuração de tempo limite de resolução infinita padrão inalterada (um valor de 0 especifica um tempo limite infinito). Isso é altamente recomendável em qualquer caso, pois os tempos limite de suporte em resoluções de nomes DNS no WinHTTP são caros em termos de desempenho. Para o Windows 2000 e posterior, a definição de um tempo limite de resolução de DNS no WinHTTP é desnecessária, pois o serviço cliente DNS subjacente implementa seu próprio tempo limite de resolução.
-   Ao processar solicitações assíncronas, o WinHTTP não manipula a representação de thread corretamente. Isso faz com que as solicitações que exigem a autenticação NTLM/Negotiate falhem, a menos que as credenciais sejam explicitamente dadas usando as funções [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) .

 

 



