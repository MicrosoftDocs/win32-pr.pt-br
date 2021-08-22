---
description: Os aplicativos que portam do WinINet para o WinHTTP podem precisar usar as mesmas configurações de reprodução automática que podem ser recuperadas em WinINet ou Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Definindo configurações de proxy WinINet no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa060d24036a02752a5eefacc9ea6672dec9bb77bad30f653c8f382490a487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133049"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Definindo configurações de proxy WinINet no WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Definindo o Proxy Automático no WinHTTP 5.1

Os aplicativos que portam do WinINet para o WinHTTP podem precisar usar as mesmas configurações de reprodução automática que podem ser recuperadas em WinINet ou Internet Explorer (IE). A API winHTTP versão 5.1 pode recuperar e usar essas configurações de proxy. Em geral, o WinHTTP especifica os servidores de bypass de proxy e proxy por sessão quando a sessão é criada. Essas configurações podem ser substituídos por solicitação.

Para usar a mesma configuração de proxy que WinINet ou IE, o cliente WinHTTP deve definir configurações de proxy para a sessão. Além disso, se o IE ou WinINet estiver configurado para usar a WPAD (Descoberta Automática de Proxy Web), o cliente WinHTTP que usa essas configurações deverá definir as configurações de proxy por solicitação. As seções a seguir descrevem como especificar as configurações de proxy para uma sessão e uma solicitação:

-   [Definindo a configuração de proxy em uma sessão](#setting-the-proxy-configuration-on-a-session)
-   [Definindo a configuração de proxy em uma única solicitação](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Definindo a configuração de proxy em uma sessão

## <a name="the-application-is-running-on-a-user-account"></a>O aplicativo está em execução em uma conta de usuário

Antes de uma sessão ser criada, o aplicativo chama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para obter as configurações de proxy do IE. O aplicativo deve estar em execução como uma conta de usuário para obter essas configurações. O parâmetro *pProxyConfig* é um ponteiro para uma estrutura [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contém o nome do proxy (*lpszProxy*) e os servidores de bypass de proxy (*lpszProxyBypass*). Os valores de bypass de proxy e nome de proxy da estrutura DE CONFIGURAÇÃO DE **\_ PROXY DE \_ \_ IE \_ \_** DO USUÁRIO ATUAL DO WINHTTP são usados para inicializar a sessão WinHTTP. A sessão é inicializada chamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) com os parâmetros *pwszProxyName* e *pwszProxyBypass* obtidos dos membros **lpszProxy** e **lpszProxyBypass** da estrutura **WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG.**

## <a name="the-application-is-running-as-a-service"></a>O aplicativo está em execução como um serviço

O aplicativo deve garantir que as configurações do Registro de um usuário individual sejam carregadas no Registro antes de chamar [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Se essas configurações não são carregadas no Registro, **WinHttpGetIEProxyConfigForCurrentUser** não poderá obter as configurações de proxy. As configurações do Registro para um usuário individual podem ser carregadas no Registro chamando a **função LoadUserProfile.** Se carregar as configurações do Registro do usuário não for uma opção, o aplicativo poderá chamar [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) com o PROXY PADRÃO DO TIPO DE **ACESSO WINHTTP \_ \_ \_ \_** especificado no parâmetro *dwAcessType.* Especificar o proxy padrão na chamada para **WinHttpOpen** informa à API WinHTTP para recuperar a configuração de proxy definida usando o utilitário winHTTP [**proxycfg.exe.**](proxycfg-exe--a-proxy-configuration-tool.md) Depois que as configurações do Registro de um usuário individual foram [](#the-application-is-running-on-a-user-account) carregadas, o aplicativo segue as etapas descritas em O aplicativo está em execução em uma conta de usuário para definir o nome do proxy e os servidores de bypass de proxy.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Definindo a configuração de proxy em uma única solicitação

Antes que a sessão seja criada, o aplicativo chama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para determinar se WinINet e IE estão configurados para usar o WPAD. **WinHttpGetIEProxyConfigForCurrentUser** retorna a estrutura [**\_ WINHTTP CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contém o **membro fAutoDetect.** Um valor **TRUE** para esse membro indica que o WPAD é usado e o membro **lpszAutoConfigUrl** contém a URL do WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>A configuração automática de proxy é usada

Se o WPAD for usado, o aplicativo [**chamará WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para recuperar o proxy para a solicitação. O *parâmetro lpwszUrl* contém a URL para a que a solicitação está sendo enviada e o parâmetro *pAutoProxyOptions* contém um ponteiro para a estrutura ([**WINHTTP \_ AUTOPROXY \_ OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) que contém as opções de reprodução automática. O aplicativo inicializa a estrutura **WINHTTP \_ AUTOPROXY \_ OPTIONS** com as configurações retornadas da estrutura [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) na chamada para [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). O sinalizador DE URL DE CONFIGURAÇÃO **WINHTTP \_ AUTOPROXY \_ \_** é especificado no membro **dwFlags** da estrutura **WINHTTP \_ AUTOPROXY \_ OPTIONS** e o membro **lpszAutoconfigUrl** contém a URL de configuração automática de proxy da estrutura DE CONFIGURAÇÃO DE PROXY DE **\_ \_ \_ IE \_ \_** DO USUÁRIO ATUAL DO WINHTTP. A **função WinHttpGetProxyForUrl** retorna o nome do proxy e a lista de bypass de proxy nos membros **lpszProxy** e **lpszProxyBypass** da estrutura [**WINHTTP \_ PROXY \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)

Depois que o proxy para a solicitação é obtido de [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), o aplicativo cria a solicitação com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Em [**seguida, WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) é chamado para definir o proxy para a solicitação especificando o handle de solicitação no *parâmetro hInternet.* O parâmetro *dwOption* na chamada para **WinHttpSetOption** deve ser definido como **\_ \_ WINHTTP OPTION PROXY** e o parâmetro *lpBuffer* é um ponteiro para uma estrutura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém o proxy e o bypass de proxy a serem usados para a solicitação.

## <a name="automatic-proxy-configuration-is-not-used"></a>A configuração automática de proxy não é usada

Se a chamada para [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indicar que a reprodução automática não é usada, o aplicativo poderá simplesmente criar a solicitação com [**WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) A configuração de proxy é a mesma para toda a sessão e as alterações por solicitação não são necessárias.

 

 



