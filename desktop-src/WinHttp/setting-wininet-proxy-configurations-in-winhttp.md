---
description: Os aplicativos que porta do WinINet para o WinHTTP talvez precisem usar as mesmas configurações de AutoProxy que podem ser recuperadas sob o WinINet ou Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Definindo as configurações de proxy do WinINet no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922779"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Definindo as configurações de proxy do WinINet no WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Definindo o proxy automático no WinHTTP 5,1

Os aplicativos que porta do WinINet para o WinHTTP talvez precisem usar as mesmas configurações de AutoProxy que podem ser recuperadas sob o WinINet ou Internet Explorer (IE). A API do WinHTTP versão 5,1 pode recuperar e usar essas configurações de proxy. Em geral, o WinHTTP especifica os servidores proxy e proxy bypass em uma base por sessão quando a sessão é criada. Essas configurações podem ser substituídas por solicitação.

Para usar a mesma configuração de proxy que o WinINet ou o IE, o cliente WinHTTP deve definir as configurações de proxy para a sessão. Além disso, se o IE ou o WinINet estiverem configurados para usar a descoberta automática de proxy da Web (WPAD), o cliente WinHTTP que usa essas configurações deve definir as configurações de proxy por solicitação. As seções a seguir descrevem como especificar as configurações de proxy para uma sessão e uma solicitação:

-   [Definindo a configuração de proxy em uma sessão](#setting-the-proxy-configuration-on-a-session)
-   [Definindo a configuração de proxy em uma única solicitação](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Definindo a configuração de proxy em uma sessão

## <a name="the-application-is-running-on-a-user-account"></a>O aplicativo está sendo executado em uma conta de usuário

Antes de uma sessão ser criada, o aplicativo chama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para obter as configurações de proxy do IE. O aplicativo deve estar sendo executado como uma conta de usuário para obter essas configurações. O parâmetro *pProxyConfig* é um ponteiro para uma estrutura de [**\_ \_ \_ \_ \_ configuração de proxy do usuário atual do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contém os servidores de nome do proxy (*lpszProxy*) e bypass do proxy (*lpszProxyBypass*). O nome do proxy e os valores de bypass do proxy da estrutura de **\_ \_ \_ \_ \_ configuração de proxy do usuário atual do WinHTTP** são usados para inicializar a sessão do WinHTTP. A sessão é inicializada chamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) com os parâmetros *pwszProxyName* e *pwszProxyBypass* obtidos dos membros **lpszProxy** e **lpszProxyBypass** da estrutura de **configuração de \_ proxy de \_ IE do usuário \_ \_ \_ atual do WinHTTP** .

## <a name="the-application-is-running-as-a-service"></a>O aplicativo está sendo executado como um serviço

O aplicativo deve garantir que as configurações do registro para um usuário individual sejam carregadas no registro antes de chamar [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Se essas configurações não forem carregadas no registro, o **WinHttpGetIEProxyConfigForCurrentUser** não poderá obter as configurações de proxy. As configurações do registro para um usuário individual podem ser carregadas no registro chamando a função **LoadUserProfile** . Se o carregamento das configurações do registro do usuário não for uma opção, o aplicativo poderá chamar [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) com o **\_ \_ \_ \_ proxy padrão do tipo de acesso WinHTTP** especificado no parâmetro *dwAcessType* . Especificar o proxy padrão na chamada para **WinHttpOpen** informa à API do WinHTTP para recuperar o conjunto de configuração de proxy usando o utilitário WinHTTP [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) . Depois que as configurações do registro de um usuário individual tiverem sido carregadas, o aplicativo seguirá as etapas descritas sob [o aplicativo que está sendo executado em uma conta de usuário](#the-application-is-running-on-a-user-account) para definir o nome do proxy e os servidores de bypass de proxy.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Definindo a configuração de proxy em uma única solicitação

Antes de a sessão ser criada, o aplicativo chama [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para determinar se o WinInet e o IE estão configurados para usar o WPAD. **WinHttpGetIEProxyConfigForCurrentUser** retorna a estrutura de [**\_ \_ \_ \_ \_ configuração do proxy IE do usuário atual do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contém o membro **fAutoDetect** . Um valor de **true** para esse membro indica que WPAD é usado e o membro **LPSZAUTOCONFIGURL** contém a URL WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>A configuração automática de proxy é usada

Se o WPAD for usado, o aplicativo chamará [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para recuperar o proxy para a solicitação. O parâmetro *lpwszUrl* contém a URL para a qual a solicitação está sendo enviada, e o parâmetro *pAutoProxyOptions* contém um ponteiro para a estrutura [**( \_ \_ Opções de proxy de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) que contém as opções de AutoProxy. O aplicativo Inicializa a estrutura de **\_ \_ Opções de AutoProxy do WinHTTP** com as configurações retornadas da estrutura de configuração de [**proxy de IE do \_ \_ usuário \_ \_ \_ atual do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) na chamada para [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). O sinalizador de **URL de \_ \_ configuração \_ de AutoProxy do WinHTTP** é especificado no membro **dwFlags** da estrutura de **\_ \_ Opções de AUTOproxy do WinHTTP** e o membro **lpszAutoconfigUrl** contém a URL de configuração automática do proxy da estrutura da configuração de **\_ \_ \_ \_ \_ proxy do usuário atual do WinHTTP** . A função **WinHttpGetProxyForUrl** retorna o nome do proxy e a lista de bypass de proxy nos membros **lpszProxy** e **lpszProxyBypass** da estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) .

Depois que o proxy para a solicitação for obtido de [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), o aplicativo criará a solicitação com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Em seguida, [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) é chamado para definir o proxy para a solicitação especificando o identificador de solicitação no parâmetro *hInternet* . O parâmetro *dwOption* na chamada a **WinHttpSetOption** deve ser definido como **\_ \_ proxy de opção WinHTTP** e o parâmetro *lpBuffer* é um ponteiro para uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém o proxy e o bypass de proxy a serem usados para a solicitação.

## <a name="automatic-proxy-configuration-is-not-used"></a>A configuração automática de proxy não é usada

Se a chamada para [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indicar que o AutoProxy não é usado, o aplicativo poderá simplesmente criar a solicitação com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). A configuração de proxy é a mesma para toda a sessão e as alterações por solicitação não são necessárias.

 

 



