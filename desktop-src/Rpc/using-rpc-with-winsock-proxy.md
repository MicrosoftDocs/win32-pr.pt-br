---
title: Usando RPC com proxy Winsock
description: Usando RPC com proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008321"
---
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="bf3e3-103">Usando RPC com proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="bf3e3-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="bf3e3-104">O lançamento do Microsoft Internet Access Server incluiu o proxy Winsock, uma versão aprimorada da API do Windows Sockets versão 1,1.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="bf3e3-105">O proxy Winsock permite que um aplicativo Windows Sockets, em execução em um cliente de rede privada, se comporte como se estivesse conectado diretamente a um aplicativo de servidor de Internet remoto.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="bf3e3-106">O servidor proxy da Microsoft atua como o host para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="bf3e3-107">Isso significa que todas as comunicações no nível do aplicativo são canalizadas por meio de um único computador protegido – o computador de gateway que executa o Microsoft Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="bf3e3-108">Normalmente, para transferências de pacote de datagrama, a DLL de transporte RPC ignora as funções [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fornecidas no Wsock32.dll e se comunica diretamente com o driver de dispositivo subjacente.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="bf3e3-109">Isso melhora a velocidade das transferências de pacote, mas torna os recursos de proxy Winsock indisponíveis para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="bf3e3-110">Cada provedor de protocolo de rede tem um GUID associado.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="bf3e3-111">A biblioteca de tempo de execução RPC compara os GUIDs UDP e IPX com os identificadores bem conhecidos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="bf3e3-112">Se eles não corresponderem, o RPC usará automaticamente o Winsock.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="bf3e3-113">Outro recurso do proxy Winsock é sua capacidade de emular o protocolo de transporte TCP no transporte do Novell SPX quando o computador cliente SPX não tiver o TCP instalado.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="bf3e3-114">Para usar esse recurso com aplicativos RPC, edite o registro do sistema em cada computador cliente para adicionar essa entrada:</span><span class="sxs-lookup"><span data-stu-id="bf3e3-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="bf3e3-115">Edite o registro em cada computador do servidor para adicionar esta entrada:</span><span class="sxs-lookup"><span data-stu-id="bf3e3-115">Edit the registry on each server computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="bf3e3-116">Para obter mais informações sobre protocolos de transporte RPC, consulte [especificando sequências de protocolo](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="bf3e3-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="bf3e3-117">Para obter mais informações sobre o proxy Winsock, consulte a documentação do produto para o Microsoft Internet Access Server.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="bf3e3-118">O Windows 2000 não implementa as entradas do registro **ClientProtocols** e **ServerProtocols** .</span><span class="sxs-lookup"><span data-stu-id="bf3e3-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="bf3e3-119">A Microsoft fornece todos os transportes bem conhecidos como parte da biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="bf3e3-120">Portanto, essas entradas não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="bf3e3-120">Therefore, these entries are not necessary.</span></span>

 

 