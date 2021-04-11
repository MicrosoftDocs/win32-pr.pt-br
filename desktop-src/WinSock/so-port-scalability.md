---
description: Habilita a escalabilidade de porta local para um soquete.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090356"
---
# <a name="so_port_scalability"></a><span data-ttu-id="c4f54-103">Portanto \_ , \_ escalabilidade de porta</span><span class="sxs-lookup"><span data-stu-id="c4f54-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="c4f54-104">A opção de soquete de **\_ \_ escalabilidade de porta,** permite a escalabilidade de porta local para um soquete.</span><span class="sxs-lookup"><span data-stu-id="c4f54-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="c4f54-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**Portanto \_ , \_ escalabilidade de porta**</span><span class="sxs-lookup"><span data-stu-id="c4f54-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f54-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="c4f54-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="c4f54-107">A opção de soquete de **\_ \_ escalabilidade de porta,** permite a escalabilidade de porta local, permitindo que a alocação de porta seja maximizada alocando portas curinga várias vezes para pares de porta de endereço local diferentes em um computador local.</span><span class="sxs-lookup"><span data-stu-id="c4f54-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4f54-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4f54-108">Remarks</span></span>

<span data-ttu-id="c4f54-109">Observação: em plataformas em que tanto \_ a \_ escalabilidade de porta quanto a \_ reutilização de \_ UNICASTPORT têm suporte, prefira usar para \_ reutilizar o \_ UNICASTPORT.</span><span class="sxs-lookup"><span data-stu-id="c4f54-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="c4f54-110">Os ambientes de servidor proxy têm problemas de escalabilidade devido à disponibilidade limitada da porta local.</span><span class="sxs-lookup"><span data-stu-id="c4f54-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="c4f54-111">Uma maneira de contornar isso é adicionar mais endereços IP ao computador.</span><span class="sxs-lookup"><span data-stu-id="c4f54-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="c4f54-112">No entanto, por padrão, as portas curinga usadas com a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) são limitadas ao tamanho do intervalo de portas dinâmicas no computador local (até 64K portas, mas geralmente menos), independentemente do número de endereços IP no computador local.</span><span class="sxs-lookup"><span data-stu-id="c4f54-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="c4f54-113">Trabalhar em conjunto com isso requer que o aplicativo Mantenha seu próprio pool de portas com a reserva de porta ou usando heurística.</span><span class="sxs-lookup"><span data-stu-id="c4f54-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="c4f54-114">Para evitar que todos os aplicativos que exigem escalabilidade gerenciem seu próprio pool de portas e para permitir maior escalabilidade enquanto mantém a compatibilidade de aplicativos, o Windows Server 2008 introduziu a opção de soquete de **\_ \_ escalabilidade de porta** para ajudar a maximizar a alocação de portas curinga.</span><span class="sxs-lookup"><span data-stu-id="c4f54-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="c4f54-115">A alocação de porta é maximizada, permitindo que um aplicativo aloque portas curinga para cada par de porta e endereço local exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c4f54-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="c4f54-116">Portanto, se um computador local tiver quatro endereços IP, até 256 de portas curinga (64 K portas × 4 endereços IP) poderão ser alocados por solicitações de função de [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) curinga.</span><span class="sxs-lookup"><span data-stu-id="c4f54-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="c4f54-117">Quando a opção de soquete de **\_ \_ escalabilidade de porta** for definida em um soquete e uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) for feita para um endereço especificado e uma porta curinga (o parâmetro *Name* for definido com um endereço específico e uma porta 0), o Winsock alocará uma porta para o endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="c4f54-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="c4f54-118">Essa alocação será baseada em todos os endereços IP e portas possíveis/por endereço no computador local.</span><span class="sxs-lookup"><span data-stu-id="c4f54-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="c4f54-119">Se uma porta curinga for adquirida usando a opção de **\_ \_ escalabilidade de porta** , essa porta não poderá ser alocada por outro soquete sem a opção de **\_ \_ escalabilidade de porta** .</span><span class="sxs-lookup"><span data-stu-id="c4f54-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="c4f54-120">Essa restrição está em vigor para evitar problemas de compatibilidade com versões anteriores com aplicativos que assumem que uma porta local curinga não pode ser reutilizada.</span><span class="sxs-lookup"><span data-stu-id="c4f54-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="c4f54-121">Observe que isso significa que os aplicativos que adquirem um grande número de portas usando a **\_ \_ escalabilidade de porta** podem não usar aplicativos herdados de portas.</span><span class="sxs-lookup"><span data-stu-id="c4f54-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="c4f54-122">Se todas as portas efêmeras disponíveis tiverem sido adquiridas para pelo menos um endereço com a **\_ \_ escalabilidade de porta** , nenhuma outra alocação de porta curinga será possível sem a opção de soquete.</span><span class="sxs-lookup"><span data-stu-id="c4f54-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="c4f54-123">Para ter qualquer efeito, a opção de **\_ \_ escalabilidade de porta de so** deve ser definida antes que a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) seja chamada.</span><span class="sxs-lookup"><span data-stu-id="c4f54-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="c4f54-124">Um exemplo de como isso seria usado em um computador com dois endereços é descrito abaixo:</span><span class="sxs-lookup"><span data-stu-id="c4f54-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="c4f54-125">A função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) é chamada por um processo para criar um soquete.</span><span class="sxs-lookup"><span data-stu-id="c4f54-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="c4f54-126">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) é chamada para habilitar a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** no soquete recém-criado.</span><span class="sxs-lookup"><span data-stu-id="c4f54-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="c4f54-127">A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada para fazer uma ligação em um dos endereços IP do computador local e na porta 0.</span><span class="sxs-lookup"><span data-stu-id="c4f54-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="c4f54-128">Em seguida, a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) é chamada para se conectar a um endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="c4f54-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="c4f54-129">O soquete é usado pelo aplicativo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c4f54-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="c4f54-130">Uma função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) é chamada pelo mesmo processo (possivelmente um thread diferente) para criar um segundo soquete.</span><span class="sxs-lookup"><span data-stu-id="c4f54-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="c4f54-131">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) é chamada para habilitar a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** no segundo soquete recém-criado.</span><span class="sxs-lookup"><span data-stu-id="c4f54-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="c4f54-132">A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada com o segundo endereço IP do computador local e a porta 0.</span><span class="sxs-lookup"><span data-stu-id="c4f54-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="c4f54-133">Mesmo quando todas as portas tiverem sido alocadas anteriormente, essa chamada terá êxito porque há vários endereços IP disponíveis no computador local e a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** foi definida em ambos os soquetes no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="c4f54-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="c4f54-134">Em seguida, a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) é chamada para se conectar a um endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="c4f54-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="c4f54-135">O segundo soquete é usado pelo aplicativo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c4f54-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f54-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4f54-136">Requirements</span></span>



| <span data-ttu-id="c4f54-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f54-137">Requirement</span></span> | <span data-ttu-id="c4f54-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c4f54-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f54-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4f54-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f54-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c4f54-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="c4f54-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4f54-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f54-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4f54-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c4f54-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4f54-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4f54-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4f54-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4f54-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4f54-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f54-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="c4f54-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="c4f54-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="c4f54-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="c4f54-148">**Opções de soquete de soquete de SOL \_**</span><span class="sxs-lookup"><span data-stu-id="c4f54-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="c4f54-149">**Opções de soquete**</span><span class="sxs-lookup"><span data-stu-id="c4f54-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




