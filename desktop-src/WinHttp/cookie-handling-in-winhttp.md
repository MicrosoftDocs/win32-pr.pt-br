---
description: Tratamento de cookies no WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Tratamento de cookies no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782512"
---
# <a name="cookie-handling-in-winhttp"></a>Tratamento de cookies no WinHTTP

Os dados da sessão HTTP são passados entre o cliente e o servidor no cabeçalho do cookie da solicitação ou da resposta. O servidor envia cookies para o cliente no cabeçalho Set-cookie da resposta e a API do WinHTTP reenvia o cookie do servidor para o servidor no cabeçalho do cookie da solicitação. As especificações de tratamento de cookies, descritas no RFC 2109 (mecanismo de gerenciamento de estado HTTP), são implementadas por padrão no WinHTTP. As especificações de tratamento de cookie recentes, descritas em RFC 2964, não são suportadas pelo WinHTTP.

O WinHTTP Obtém o cookie do cabeçalho Set-Cookie de servidores e o armazena em um cache por sessão. Esse cookie é reenviado em solicitações subsequentes na mesma sessão do WinHTTP em que o destino corresponde à origem do cookie. A API do WinHTTP regenera o cabeçalho de cookie de solicitação para cada segmento na solicitação.

A lista a seguir descreve várias opções que os aplicativos cliente WinHTTP podem usar para lidar com cookies:

-   Tratamento automático de cookies-o WinHTTP manipula automaticamente os cookies e o aplicativo cliente não executa nenhuma manipulação de cookie personalizada.
-   Desabilitar o tratamento automático de cookies-o tratamento automático de cookies na API do WinHTTP está desabilitado e nenhum cookie é enviado.
-   Especificar manualmente todos os cookies – o tratamento automático de cookies está desabilitado e o aplicativo cliente adiciona ou remove todos os cabeçalhos de cookie de cada solicitação na sessão.
-   Manipulação manual e automática de cookies – Combine manipulação automática e manual de cookies.

## <a name="disabling-automatic-cookie-handling"></a>Desabilitando a manipulação automática de cookies

Para desabilitar a manipulação de cookies, o aplicativo cliente WinHTTP chama a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com o parâmetro *dwOption* definido como \_ opção WinHTTP \_ Disable \_ Feature e o parâmetro *lpBuffer* definido como WinHTTP \_ Disable \_ cookies. O parâmetro *hInternet* pode ser um identificador de sessão ou um identificador de solicitação. Quando o tratamento de cookies é desabilitado em um identificador de solicitação que enviou uma solicitação anterior, o cliente deve remover manualmente os cabeçalhos de cookie de solicitação existentes com a função [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) antes de enviar a próxima solicitação. Para obter mais informações, consulte [removendo cabeçalhos de cookie](#removing-cookie-headers).

**Observação**  O aplicativo cliente deve definir todos os cookies na sessão após o modo automático ter sido desabilitado.

## <a name="manually-specifying-all-cookies"></a>Especificando manualmente todos os cookies

Quando o tratamento automático de cookies está desabilitado, o aplicativo cliente WinHTTP tem a opção de especificar manualmente todos os cookies. Para definir manualmente o cookie, o aplicativo chama [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) especificando o cabeçalho do cookie no parâmetro *pwszHeaders* . O aplicativo cliente deve limpar todos os cabeçalhos de cookie antes de reenviar a solicitação.

O aplicativo cliente também deve alterar o cabeçalho do cookie quando a solicitação for redirecionada. Para alterar o cookie em solicitações redirecionadas, o cliente especifica uma função de retorno de chamada com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde ao caso de retorno de chamada de redirecionamento. O manipulador de retorno de chamada deve limpar o cookie enviado anteriormente na solicitação chamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Para obter mais informações sobre como remover cabeçalhos de cookie, consulte [removendo cabeçalhos de cookie](#removing-cookie-headers).

## <a name="manual-and-automatic-cookie-handling"></a>Manipulação manual e automática de cookies

Os aplicativos cliente WinHTTP podem combinar o mecanismo de tratamento automático de cookies do WinHTTP com manipulação manual de cookies. O aplicativo adiciona cookies personalizados ao cabeçalho de cookie gerado automaticamente antes de enviar a solicitação com a função [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) . O cookie personalizado deve ser o primeiro cabeçalho de cookie na solicitação para que a API do WinHTTP armazene corretamente o cookie em cache. O aplicativo cliente também deve remover cookies enviados em solicitações anteriores antes de reenviar uma solicitação no mesmo identificador de solicitação. Para obter mais informações, consulte Removendo cabeçalhos de cookie.

Os cookies adicionados a uma solicitação antes que a chamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sejam incluídas em todas as solicitações de WinHTTP enviadas em nome das próximas chamadas de **WinHttpSendRequest** e [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . O aplicativo cliente pode precisar limpar o cabeçalho do cookie quando a solicitação for redirecionada. Para limpar o cookie em solicitações redirecionadas, o cliente especifica uma função de retorno de chamada com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde ao caso de retorno de chamada de redirecionamento. O manipulador de retorno de chamada deve limpar o cookie que foi enviado anteriormente na solicitação chamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). A função de retorno de chamada não pode definir novos cookies personalizados no retorno de chamada de redirecionamento. O cliente deve aguardar a conclusão do **WinHttpReceiveResponse** antes de adicionar novos cookies para a próxima chamada **WinHttpSendRequest** .

## <a name="removing-cookie-headers"></a>Removendo cabeçalhos de cookie

O aplicativo cliente WinHTTP pode precisar limpar o cookie de solicitação existente antes de reenviar uma solicitação para impedir que cookies enviados em solicitações anteriores sejam enviados novamente na solicitação atual; para obter mais informações, consulte a observação a seguir. Além disso, lembre-se de que os cookies não precisam ser limpos antes que a primeira solicitação seja enviada no identificador de solicitação. O cliente pode limpar os cookies existentes chamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) com um cabeçalho de cookie vazio no parâmetro *pwszHeaders* e o \_ sinalizador de substituição do sinalizador WinHTTP ADDREQ \_ \_ definido no parâmetro *dwModifier* . O exemplo de código a seguir mostra como limpar o cabeçalho do cookie na solicitação.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

A API do WinHTTP tem comportamentos de manipulação de cookies diferentes para versões do sistema operacional anteriores ao Windows XP com Service Pack 2 (SP2) e Windows Server 2003 com Service Pack 1 (SP1).

* * Windows XP com SP2 e posterior e Windows Server 2003 com SP1 e posterior: * *

A API do WinHTTP limpa todos os cookies enviados em solicitações anteriores para o identificador de solicitação. O cliente pode adicionar manualmente novos cabeçalhos de cookie antes de cada chamada para WinHttpSendRequest. Se a funcionalidade de manipulação automática de cookies da API do WinHTTP não tiver sido desabilitada, a API do WinHTTP acrescentará o novo cabeçalho de cookie (ou adicionará um novo cabeçalho de cookie se o aplicativo cliente não tiver adicionado um manualmente) com o cookie do servidor.

* * Windows XP com SP2 e Windows Server 2003 com SP1: * *

A API do WinHTTP não limpa o cabeçalho de cookie de solicitação após a conclusão do [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . Os cookies enviados em solicitações anteriores serão reenviados em chamadas subsequentes para [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). O aplicativo cliente WinHTTP deve limpar os cabeçalhos de cookies existentes antes de reenviar uma solicitação no identificador de solicitação.

 

 



