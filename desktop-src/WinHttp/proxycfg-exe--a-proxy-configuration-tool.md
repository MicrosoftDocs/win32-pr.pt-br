---
description: Este tópico explica o uso da ferramenta de configuração de proxy do Microsoft Windows HTTP Services (WinHTTP), &\# 0034; ProxyCfg.exe&\# 0034;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Ferramentas de Configuração de proxy de Netsh.exe e ProxyCfg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501247"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Ferramentas de Configuração de proxy de Netsh.exe e ProxyCfg.exe

* * Windows Vista e Windows Server 2008: * *

ProxyCfg.exe foi preterido. Ele é substituído pelos comandos [Netsh.exe WinHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) .

Este tópico explica o uso da ferramenta de configuração de proxy do [Microsoft Windows http Services (WinHTTP)](about-winhttp.md) , "ProxyCfg.exe".

Há duas maneiras de acessar servidores HTTP e HTTPS (protocolo de transferência de hipertexto) seguros por meio de um proxy usando o Microsoft Windows HTTP Services (WinHTTP). Primeiro, você pode especificar as configurações de proxy de dentro de seu aplicativo WinHTTP. Em segundo lugar, você pode especificar as configurações de proxy padrão de fora do seu aplicativo usando o utilitário de configuração de proxy localizado no diretório% windir% \\ System32.

Você pode definir programaticamente os dados de proxy de dentro de seu aplicativo ou script. Se você estiver escrevendo um aplicativo usando a API do WinHTTP, use uma das duas técnicas a seguir para alterar as configurações de proxy.

-   Use a função [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . Especifique o tipo de acesso no segundo parâmetro, o nome do proxy no terceiro parâmetro e uma lista de bypass no quarto parâmetro. O exemplo a seguir mostra como a função [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) pode ser usada para definir dados de proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Use a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) . O sinalizador de [**\_ \_ proxy de opção WinHTTP**](option-flags.md) permite que você especifique as configurações de proxy com uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) . O código de exemplo a seguir mostra como a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pode ser usada para definir dados de proxy.

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

Se você estiver escrevendo um script ou um aplicativo usando o objeto [**WinHttpRequest**](winhttprequest.md) , use a técnica a seguir para alterar as configurações de proxy.

-   Use o método [**SetProxy**](iwinhttprequest-setproxy.md) . Especifique o tipo de acesso no primeiro parâmetro, o nome do proxy no segundo parâmetro e uma lista de bypass no terceiro parâmetro. O exemplo a seguir mostra como o método [**SetProxy**](iwinhttprequest-setproxy.md) pode ser usado no script para definir dados de proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Para especificar as configurações padrão e eliminar a necessidade de usar o método [**SetProxy**](iwinhttprequest-setproxy.md) ou a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , use o utilitário de configuração de proxy. Usando esse utilitário, você pode especificar que seu aplicativo acesse uma rede diretamente, por meio de um proxy ou por meio de uma combinação de acesso direto e de proxy, especificando uma lista de bypass. Quando você usa a API do WinHTTP, a ferramenta de configuração de proxy determina apenas as configurações quando você passa o sinalizador **padrão de \_ tipo de acesso \_ \_ WinHTTP** para a API [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . O objeto [**WinHttpRequest**](winhttprequest.md) usa as configurações da ferramenta de configuração de proxy por padrão.

As configurações de proxy para WinHTTP não são as configurações de proxy do Microsoft Internet Explorer. Você não pode definir as configurações de proxy para WinHTTP no painel de controle do Microsoft Windows. Usar o utilitário de configuração de proxy WinHTTP não altera as configurações usadas para o Internet Explorer.

> [!Note]  
> Se você tentar abrir e enviar uma solicitação HTTP usando o WinHTTP e as configurações de proxy estiverem incorretas, ocorrerá um erro.

 

## <a name="command-line-parameters"></a>Parâmetros de linha de comando

A tabela a seguir lista os parâmetros de linha de comando disponíveis para uso com a ferramenta ProxyCfg.exe.



| Parâmetro | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nenhum      | Quando nenhum parâmetro é especificado, as configurações de proxy do WinHTTP atuais são exibidas.                                                                                                                                                                                                                                                                                                                                               |
| ?         | As informações de ajuda são exibidas.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Especifica que os aplicativos WinHTTP acessam a rede diretamente, sem um proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Especifica o servidor proxy. Você também pode especificar uma lista opcional de servidores que são acessados sem um proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Especifica que os aplicativos WinHTTP usam as configurações de proxy do usuário atual para o Internet Explorer. Esse parâmetro não funcionará se o Internet Explorer estiver detectando automaticamente as configurações de proxy ou se estiver usando uma URL de configuração automática para definir as informações de proxy.                                                                                                                                                      |
| i         | Especifica que os aplicativos WinHTTP usam as configurações de proxy do usuário atual para o Internet Explorer. Isso só funciona quando ProxyCfg.exe não foi usado anteriormente. Se ProxyCfg.exe estiver instalado, especifique que o parâmetro de linha de comando "u" Use as configurações manuais. Esse parâmetro não funcionará se o Internet Explorer detectar automaticamente as configurações de proxy ou se usar uma URL de configuração automática para definir as informações de proxy. |



 

Você pode especificar proxies em uma cadeia de caracteres delimitada por espaço. As listagens de proxy podem conter o número da porta usado para acessar o proxy. Para listar um proxy para um protocolo específico, a cadeia de caracteres deve seguir o formato, <protocol> = https://<nome do proxy \_>. Os protocolos válidos são HTTP e HTTPS. Por exemplo, para listar um proxy HTTP, uma cadeia de caracteres válida é http = https://http\_proxy\_name:80 , em que o \_ \_ nome do proxy http é o nome do servidor proxy e 80 é o número da porta que você deve usar para acessar o proxy. Se o proxy usar o número da porta padrão para esse protocolo, você poderá omitir o número da porta. Se um nome de proxy estiver listado por si só, você poderá usá-lo como o proxy padrão para qualquer protocolo que não tenha um proxy especificado. Por exemplo, http = https://http\_proxy outro \_ proxy usa \_ proxy http para qualquer operação http, enquanto o protocolo HTTPS usa o proxy chamado outro \_ proxy.

Você pode listar os nomes de host ou endereços IP conhecidos localmente na lista de bypass de proxy. Essa lista pode conter curingas, como " \* ", que fazem com que o aplicativo ignore o servidor proxy para endereços que se ajustam ao padrão especificado, por exemplo, " \* . Microsoft.com" ou " \* . org". Os caracteres curinga devem ser os caracteres mais à esquerda na lista. Por exemplo, "AAA \* ". Não tem suporte. Para listar vários endereços e nomes de host, separe-os com espaços em branco ou pontos-e-vírgulas na cadeia de caracteres de bypass de proxy. Se você especificar a <local> macro, a função ignorará qualquer nome de host que não contenha um ponto.

> [!WARNING]
> Depois que Proxycfg.exe for executado, você não poderá restaurar as configurações de proxy anteriores. No entanto, você pode remover totalmente as configurações de proxy.

 

## <a name="usage"></a>Uso

Para usar a ferramenta de configuração de proxy, abra uma janela de prompt de comando e execute o utilitário de configuração de proxy com os parâmetros de linha de comando apropriados. A seção a seguir fornece exemplos de sintaxe.

## <a name="example-syntax"></a>Sintaxe de exemplo

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Exemplo 1: usar um proxy somente para recursos externos

Veja a seguir o uso mais comum para Proxycfg.exe. Esse comando especifica que os servidores HTTP e HTTPS são acessados por meio do servidor proxy chamado " \_ servidor proxy", exceto nomes de host que não contêm um ponto.

**servidor proxy proxycfg-p \_ " <local> "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Exemplo 2: usar um proxy para todos os recursos

O exemplo a seguir especifica que os servidores HTTP e HTTPS são acessados por meio do servidor proxy chamado " \_ servidor proxy". Nenhuma lista de bypass foi especificada.

**servidor proxy proxycfg-p \_**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Exemplo 3: usar um proxy diferente para recursos seguros

O exemplo a seguir especifica que os servidores HTTP são acessados por meio do \_ proxy de proxy http e os servidores HTTPS são acessados por meio do \_ proxy HTTPS. Os sites de intranet local e qualquer site no \* domínio. Microsoft.com ignoram o proxy.

**proxycfg-p "http = http \_ proxy HTTPS = \_ proxy HTTPS" " <local> ; \* . microsoft.com "**

## <a name="removing-proxycfgexe"></a>Removendo ProxyCfg.exe

Depois de usar a ferramenta de configuração de proxy, você não pode restaurar suas configurações de proxy originais. No entanto, se necessário, você pode remover as configurações do registro que o utilitário cria. Para remover as entradas do registro que ProxyCfg.exe cria, você deve excluir o valor de **WinHttpSettings** da seguinte chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings** \\ **Connections** \\ **WinHttpSettings**

Excluir o valor *WinHttpSettings* remove todas as configurações de proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe e autenticação

O utilitário de configuração de proxy define a política de autenticação padrão. Como você não deve executar a autenticação NTLM com hosts não confiáveis, por padrão, a autenticação NTLM ocorre apenas automaticamente com hosts na lista de bypass de proxy. Se não houver nenhum proxy, você ainda poderá usar ProxyCfg.exe para especificar uma lista de bypass de hosts em que você confia para executar a autenticação NTLM. Um nome de proxy é necessário ao usar ProxyCfg.exe para essa finalidade, mas você pode usar qualquer cadeia de caracteres válida no lugar de um nome de proxy real.

Para obter mais informações sobre a política de logon automático, consulte [política de logon automático](authentication-in-winhttp.md).

 

 
