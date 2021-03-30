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
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640859"
---
# <a name="ncacn_http-attribute"></a><span data-ttu-id="509b1-104">\_atributo http ncacn</span><span class="sxs-lookup"><span data-stu-id="509b1-104">ncacn\_http attribute</span></span>

<span data-ttu-id="509b1-105">A palavra-chave **\_ http ncacn** identifica o IIS (Microsoft Internet Information Server) como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="509b1-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="509b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="509b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="509b1-107">*\_servidor RPC*</span><span class="sxs-lookup"><span data-stu-id="509b1-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="509b1-108">O endereço da Internet ou o nome do computador no qual o processo do servidor RPC está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="509b1-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="509b1-109">*extremidade*</span><span class="sxs-lookup"><span data-stu-id="509b1-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="509b1-110">A porta TCP/IP bem conhecida (estática) em que o processo do servidor RPC está escutando.</span><span class="sxs-lookup"><span data-stu-id="509b1-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="509b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="509b1-111">Remarks</span></span>

<span data-ttu-id="509b1-112">Identificar o IIS (Microsoft Internet Information Server) como a família de protocolos permite que aplicativos cliente e servidor se comuniquem pela Internet usando o IIS (Microsoft Internet Information Server) como um proxy.</span><span class="sxs-lookup"><span data-stu-id="509b1-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="509b1-113">Como as chamadas são encapsuladas por meio de uma porta HTTP estabelecida, elas podem atravessar firewalls.</span><span class="sxs-lookup"><span data-stu-id="509b1-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="509b1-114">Qualquer cliente RPC e aplicativos de servidor podem dar suporte ao protocolo **\_ http ncacn** , desde que eles estejam em rede a um servidor de informações da Internet.</span><span class="sxs-lookup"><span data-stu-id="509b1-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="509b1-115">O IIS entra em contato com o servidor RPC e estabelece um soquete TCP/IP, que ele mantém para o cliente.</span><span class="sxs-lookup"><span data-stu-id="509b1-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="509b1-116">O IIS negocia uma conexão TCP/IP com o servidor RPC e, quando a negociação é concluída, atua como um proxy RPC, encaminhando dados entre o soquete TCP/IP do lado do cliente e o soquete TCP/IP do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="509b1-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="509b1-117">Quando o proxy RPC do IIS detecta um fechamento de sessão no cliente ou no lado do servidor, ele fecha o soquete restante.</span><span class="sxs-lookup"><span data-stu-id="509b1-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="509b1-118">O aplicativo cliente usa implicitamente a associação estática para o IIS, mas o servidor pode usar pontos de extremidade dinâmicos, com RPCSs do servidor (mapeador de ponto de extremidade) resolvendo a porta do servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="509b1-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="509b1-119">Se o IIS estiver em um computador diferente do servidor RPC, o IIS receberá a chamada remota, entrará em contato com RPCSs no computador do servidor RPC para obter o ponto de extremidade do processo do servidor e, em seguida, encaminha a chamada para o servidor RPC apropriado.</span><span class="sxs-lookup"><span data-stu-id="509b1-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="509b1-120">Se o Internet Explorer estiver instalado, o transporte verificará o registro para ver se há uma configuração para um proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="509b1-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="509b1-121">Se um proxy existir, o transporte o usará.</span><span class="sxs-lookup"><span data-stu-id="509b1-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="509b1-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="509b1-122">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="509b1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="509b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509b1-124">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="509b1-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="509b1-125">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="509b1-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="509b1-126">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="509b1-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 