---
description: Página de navegação para opções de soquete do Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opções de soquete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762181"
---
# <a name="socket-options"></a><span data-ttu-id="b943a-103">Opções de soquete</span><span class="sxs-lookup"><span data-stu-id="b943a-103">Socket Options</span></span>

<span data-ttu-id="b943a-104">Esta seção descreve as opções de soquete do Winsock para várias edições de sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="b943a-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="b943a-105">Use as funções [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter e definir opções de soquete.</span><span class="sxs-lookup"><span data-stu-id="b943a-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="b943a-106">Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="b943a-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="b943a-107">Algumas opções de soquete exigem mais explicações do que essas tabelas podem ser transmitidas; essas opções contêm links para páginas adicionais.</span><span class="sxs-lookup"><span data-stu-id="b943a-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="b943a-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="b943a-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-109">Opções de soquete aplicáveis no nível de IPv4.</span><span class="sxs-lookup"><span data-stu-id="b943a-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="b943a-110">Para obter mais informações, consulte [**as \_ Opções de soquete de IP do IPPROTO**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="b943a-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-112">Opções de soquete aplicáveis no nível de IPv6.</span><span class="sxs-lookup"><span data-stu-id="b943a-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="b943a-113">Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO IPv6**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**</span><span class="sxs-lookup"><span data-stu-id="b943a-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-115">Opções de soquete aplicáveis no nível de multicast confiável.</span><span class="sxs-lookup"><span data-stu-id="b943a-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="b943a-116">Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO RM**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="b943a-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-118">Opções de soquete aplicáveis no nível de TCP.</span><span class="sxs-lookup"><span data-stu-id="b943a-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="b943a-119">Para obter mais informações, consulte [**as \_ Opções de soquete TCP IPPROTO**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="b943a-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-121">Opções de soquete aplicáveis no nível de UDP.</span><span class="sxs-lookup"><span data-stu-id="b943a-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="b943a-122">Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO UDP**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="b943a-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-124">Opções de soquete aplicáveis no nível de IPX.</span><span class="sxs-lookup"><span data-stu-id="b943a-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="b943a-125">Para obter mais informações, consulte [**as \_ Opções de soquete IPX NSPROTO**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL para o \_ APPLETALK**</span><span class="sxs-lookup"><span data-stu-id="b943a-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-127">Opções de soquete aplicáveis no nível de AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="b943a-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="b943a-128">Para obter mais informações, consulte [**as \_ Opções de soquete do sol**](sol-appletalk-socket-options.md)</span><span class="sxs-lookup"><span data-stu-id="b943a-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**</span><span class="sxs-lookup"><span data-stu-id="b943a-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-130">Opções de soquete aplicáveis ao nível do protocolo de gerenciamento de link de infravermelho.</span><span class="sxs-lookup"><span data-stu-id="b943a-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="b943a-131">Para obter mais informações, consulte [**as \_ Opções de soquete sol IRLMP**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b943a-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**soquete de SOL \_**</span><span class="sxs-lookup"><span data-stu-id="b943a-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b943a-133">Opções de soquete aplicáveis no nível do soquete.</span><span class="sxs-lookup"><span data-stu-id="b943a-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="b943a-134">Para obter mais informações, consulte [**as \_ Opções de soquete de soquete de sol**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="b943a-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b943a-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="b943a-135">Remarks</span></span>

<span data-ttu-id="b943a-136">Todas as \_ \* Opções de soquete se aplicam igualmente ao IPv4 e ao IPv6 (exceto por \_ difusão, já que a difusão não é implementada no IPv6).</span><span class="sxs-lookup"><span data-stu-id="b943a-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



