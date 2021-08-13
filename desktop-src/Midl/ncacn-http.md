---
title: ncacn_http atributo
description: A \_ palavra-chave http ncacn identifica o IIS (Microsoft Internet Information Server) como a família de protocolos para o ponto de extremidade.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7eed41849f59e497000e9ad56ae7c3166cf2d0212986fa9ba5f5ea910ed364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642207"
---
# <a name="ncacn_http-attribute"></a>\_atributo http ncacn

A palavra-chave **\_ http ncacn** identifica o IIS (Microsoft Internet Information Server) como a família de protocolos para o ponto de extremidade.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\_servidor RPC* 
</dt> <dd>

O endereço da Internet ou o nome do computador no qual o processo do servidor RPC está sendo executado.

</dd> <dt>

*endpoint* 
</dt> <dd>

A porta TCP/IP bem conhecida (estática) em que o processo do servidor RPC está escutando.

</dd> </dl>

## <a name="remarks"></a>Comentários

Identificar o IIS (Microsoft Internet Information Server) como a família de protocolos permite que aplicativos cliente e servidor se comuniquem pela Internet usando o IIS (Microsoft Internet Information Server) como um proxy. Como as chamadas são encapsuladas por meio de uma porta HTTP estabelecida, elas podem atravessar firewalls.

Qualquer cliente RPC e aplicativos de servidor podem dar suporte ao protocolo **\_ http ncacn** , desde que eles estejam em rede a um servidor de informações da Internet. O IIS entra em contato com o servidor RPC e estabelece um soquete TCP/IP, que ele mantém para o cliente. O IIS negocia uma conexão TCP/IP com o servidor RPC e, quando a negociação é concluída, atua como um proxy RPC, encaminhando dados entre o soquete TCP/IP do lado do cliente e o soquete TCP/IP do lado do servidor. Quando o proxy RPC do IIS detecta um fechamento de sessão no cliente ou no lado do servidor, ele fecha o soquete restante.

O aplicativo cliente usa implicitamente a associação estática para o IIS, mas o servidor pode usar pontos de extremidade dinâmicos, com RPCSs do servidor (mapeador de ponto de extremidade) resolvendo a porta do servidor RPC. Se o IIS estiver em um computador diferente do servidor RPC, o IIS receberá a chamada remota, entrará em contato com RPCSs no computador do servidor RPC para obter o ponto de extremidade do processo do servidor e, em seguida, encaminha a chamada para o servidor RPC apropriado.

Se o Internet Explorer estiver instalado, o transporte verificará o registro para ver se há uma configuração para um proxy HTTP. Se um proxy existir, o transporte o usará.

## <a name="examples"></a>Exemplos

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 