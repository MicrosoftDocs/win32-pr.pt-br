---
title: Usando HTTP como um transporte RPC
description: RPC via HTTP permite que os programas cliente usem a Internet para executar procedimentos fornecidos por programas de servidor em redes distantes.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5860757a6c5df9937e77fc078df2526affb967fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453627"
---
# <a name="using-http-as-an-rpc-transport"></a>Usando HTTP como um transporte RPC

RPC via HTTP permite que os programas cliente usem a Internet para executar procedimentos fornecidos por programas de servidor em redes distantes. O RPC sobre HTTP encapsula suas chamadas por meio de uma porta HTTP estabelecida. Portanto, suas chamadas podem atravessar firewalls de rede nas redes de cliente e servidor.

O RPC sobre HTTP roteia suas chamadas para o proxy RPC localizado na rede do servidor RPC. O proxy RPC estabelece e mantém uma conexão com o servidor RPC. Ele serve como um proxy, expedindo chamadas de procedimento remoto para o servidor RPC e enviando as respostas do servidor de volta pela Internet para o aplicativo cliente. Esse processo é ilustrado no diagrama a seguir.

![interação entre um servidor RPC e o Internet Information Server para RPC http](images/httprpc1.png)

O diagrama mostra um firewall na rede do aplicativo cliente. Isso não é necessário para que o RPC sobre HTTP opere. No entanto, se a rede do cliente tiver um firewall, ele também precisará de um programa de servidor proxy, como o Microsoft Proxy Server.

Quando o programa cliente emite uma chamada de procedimento remoto usando HTTP como o transporte, a biblioteca de tempo de execução RPC no cliente entra em contato com o proxy RPC. Dependendo se o cliente RPC foi solicitado a usar a porta HTTP ou HTTPS (HTTP com SSL) 80 ou a porta 443 é usada, respectivamente. O proxy RPC entra em contato com o programa do servidor RPC e estabelece uma conexão TCP/IP. O cliente e o proxy RPC mantêm sua conexão HTTP ou HTTPS pela Internet. A conexão HTTP ou HTTPS do cliente para o proxy RPC pode passar por um firewall (sujeito às permissões de acesso apropriadas) se houver um. Em seguida, o servidor pode executar a chamada de procedimento remoto e usar a conexão por meio do proxy RPC para responder ao cliente. O proxy RPC é uma extensão ISAPI em execução no contexto do IIS.

Se o cliente ou o servidor se desconectar por qualquer motivo, o proxy RPC irá detectá-lo e encerrar a sessão RPC. Desde que a sessão continue, o proxy RPC manterá suas conexões com o cliente e o servidor. Ele encaminhará chamadas de procedimento remoto do cliente para o servidor e enviará respostas do servidor para o cliente.

O programa cliente RPC pode encapsular suas chamadas RPC pela Internet criando uma associação de cadeia de caracteres no formato:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Em que:

-   *o \_ UUID do objeto* especifica um UUID do objeto RPC. Para obter mais informações, consulte [gerando UUIDs de interface](generating-interface-uuids.md) e [UUID de cadeia de caracteres](string-uuid.md).
-   **ncacn \_ http** seleciona a especificação de sequência de protocolo para RPC sobre http. Para obter mais informações, consulte [constantes de sequência de protocolo](protocol-sequence-constants.md) e Associação de cadeia de [caracteres](string-binding.md).
-   *\_ servidor RPC* é o endereço de rede do computador que está executando o processo do servidor RPC. O endereço do servidor deve ser especificado em um formulário visível e compreensível pelo computador do proxy RPC, não pelo cliente. Como o cliente não se conecta diretamente ao servidor, ele não precisa ser capaz de resolver o nome do servidor ou estabelecer uma conexão com ele. O proxy RPC estabelecerá a conexão em nome do cliente e, portanto, o *\_ servidor RPC* deverá ser um nome reconhecível pelo proxy RPC.
-   *ponto de extremidade* especifica a porta TCP/IP que o processo do servidor RPC escuta para chamadas de procedimento remoto. Para obter mais informações, consulte [localizando pontos de extremidade](finding-endpoints.md).
-   O **HttpProxy** opcionalmente especifica um servidor proxy http na rede do cliente RPC, como o Microsoft Proxy Server. Se um servidor proxy for selecionado, nenhum número de porta será especificado, o stub de RPC usará a porta 80 por padrão se o SSL não for solicitado e a porta 443 se o SSL for especificado.
-   O **RpcProxy** especifica o endereço e o número da porta do computador IIS que atua como um proxy para o servidor RPC. Você só precisará especificar isso se o processo do servidor RPC residir em um computador diferente do proxy RPC. Se você não especificar um número de porta, o stub de cliente RPC usará a porta 80 se o SSL não for especificado e usará a porta 443 se o SSL (HTTPS) for especificado.
-   O **HttpConnectionOption** opcionalmente permite direcionar o comportamento do RPC ao fazer conexões http. O valor **UseHttpProxy** INSTRUI o RPC a rotear seu tráfego por meio do proxy http em todos os momentos, incluindo quando o cliente tem suas opções de Internet definidas no Internet Explorer como "ignorar servidor proxy para endereços locais".

    Essa opção tem suporte no Windows 7, Windows Server 2008 R2, Windows 8.1 e Windows Server 2012 R2 com KB2916915 instalado. Não há suporte para essa opção no Windows 8 e no Windows Server 2012. Os aplicativos podem determinar se essa opção é suportada pelo tempo de execução RPC, verificando o valor do registro **ConnectionOptionsFlag** localizado na seguinte chave do registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC**

    Se o bit 0 (LSB) desse valor de registro for definido, essa opção específica terá suporte; caso contrário, essa opção não é suportada pelo tempo de execução RPC no sistema.

Para obter mais informações sobre como criar associações de cadeia de caracteres, consulte [Binding e Handles](binding-and-handles.md).

O programa do servidor RPC pode aceitar chamadas RPC em túnel ouvindo na sequência de \_ protocolo http ncacn.

A Microsoft tem duas implementações principais do RPC sobre HTTP: versão 1 e versão 2.

A versão 1 (chamada RPC sobre HTTP v1) tem suporte por meio do Windows XP. A versão 1 do proxy RPC tem suporte por meio do Windows 2000.

A versão 2 (chamada RPC sobre HTTP v2) é a versão atual.

As duas versões têm diferentes recursos e interoperabilidade limitada. Um resumo das diferenças é fornecido aqui. Para considerações sobre interoperabilidade, consulte [requisitos do sistema e interoperabilidade para RPC sobre http](system-requirements-and-interoperability-for-rpc-over-http.md).

-   RPC sobre HTTP v1 requer que o túnel SSL seja habilitado em todos os proxies/firewalls HTTP entre o cliente RPC sobre HTTP e o proxy RPC. O RPC sobre HTTP v1 tenta criar um túnel SSL pela porta 80, embora os dados enviados por ele não sejam criptografados por SSL. Os proxies e os firewalls geralmente rejeitam essas solicitações, a menos que sejam explicitamente configuradas para permiti-las. RPC sobre HTTP v2 não tem tal requisito.
-   RPC sobre HTTP v1 não pode estabelecer uma sessão SSL para o proxy RPC. O RPC sobre HTTP V2 pode enviar todo o tráfego RPC sobre HTTP dentro de uma sessão SSL; Por padrão v2 exige que os dados sejam enviados em uma sessão SSL.
-   RPC sobre HTTP v1 não pode autenticar no proxy RPC. RPC sobre HTTP V2 pode autenticar; Por padrão, v2 requer autenticação para o proxy RPC.
-   O proxy RPC v1 não funciona corretamente quando o computador IIS no qual ele está instalado faz parte de um web farm. O proxy RPC v2 funciona corretamente quando o computador IIS no qual ele está instalado faz parte de um web farm.

> [!Note]  
> Se o Microsoft Internet Explorer estiver instalado no computador do programa cliente e o cliente não especificar um **HttpProxy** em sua associação de cadeia de caracteres, o stub do cliente RPC pesquisará o registro no computador cliente em busca de uma entrada **HttpProxy** . Se encontrar um, ele usará o proxy especificado na entrada do registro.

 

Suponha, por exemplo, que o programa cliente precise se conectar pela Internet a um servidor RPC em um computador chamado Server7.microsoft.com. Além disso, suponha que o proxy RPC seja executado em Major7.microsoft.com. O programa do servidor RPC escuta a porta 2225. O cliente usaria a associação de cadeia de caracteres:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Se o proxy RPC puder resolver o nome do servidor como Server7, sem a necessidade de um nome de domínio totalmente qualificado, você também poderá especificar:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Se a rede do cliente usar um firewall e um servidor proxy da Internet chamado MyProxy e o Internet Explorer no cliente não estiver configurado para usar esse proxy, você precisará modificar a associação de cadeia de caracteres do cliente para:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Isso instrui o cliente a se conectar ao programa de servidor RPC no Server7.microsoft.com. Para fazer isso, o cliente usará primeiro a porta 80 (ou a porta 443 se o SSL for usado) para se conectar a MyProxy. Isso fornecerá ao programa cliente acesso à Internet. Usando a Internet, o programa cliente se conecta ao proxy RPC em Major7.microsoft.com. O proxy RPC estabelecerá uma conexão com o programa do servidor RPC em execução no Server7.microsoft.com.

Se a rede do cliente usar um firewall e se o proxy RPC não puder ser acessado diretamente, para obter uma conexão estabelecida mais rapidamente, a associação de cadeia de caracteres do cliente poderá ser modificada para:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

O **HttpConnectionOption** permite direcionar o comportamento do RPC ao fazer conexões http. O valor **UseHttpProxy** INSTRUI o RPC a rotear seu tráfego por meio do proxy http em todos os momentos, incluindo quando o cliente tem suas opções de Internet definidas no Internet Explorer como "ignorar servidor proxy para endereços locais". Isso instrui o cliente a se conectar de modo forçado ao proxy RPC por meio do proxy http. Isso acelera o tempo para estabelecer uma conexão, já que ignora qualquer atraso na pesquisa do servidor RPC diretamente antes de usar o proxy HTTP.

Se a opção **HttpConnectionOption** for usada e o Internet Explorer no cliente não estiver configurado para usar esse proxy http, as conexões poderão falhar **com \_ Opções de \_ \_ rede \_ RPC S inválidas**.

A grande maioria dos computadores hoje está configurada para navegação na Web. Portanto, a maioria dos clientes não precisa especificar o **HttpProxy**, pois ele será recuperado das configurações de conectividade da Internet.

 

 




