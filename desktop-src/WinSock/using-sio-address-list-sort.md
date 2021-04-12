---
description: O IOCTL de classificação da lista de endereços do SIO \_ \_ \_ permite que os desenvolvedores de aplicativos classifiquem uma lista de endereços de destino IPv6 e IPv4 para determinar o melhor endereço disponível para fazer uma conexão. O \_ IOCTL de classificação da lista de endereços sio \_ \_ tem suporte no Windows XP e versões posteriores.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Usando SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171467"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="3f28c-104">Usando a \_ \_ classificação da lista de endereços do sio \_</span><span class="sxs-lookup"><span data-stu-id="3f28c-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="3f28c-105">O IOCTL de classificação da lista de endereços do sio permite que os desenvolvedores de aplicativos classifiquem uma lista de endereços de destino IPv6 e IPv4 para determinar o melhor endereço disponível para fazer uma conexão. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f28c-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="3f28c-106">O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** tem suporte no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3f28c-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="3f28c-107">No Windows Vista e posterior, a função [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) usa uma lista fornecida de possíveis endereços IP de destino, emparelha os endereços de destino com os endereços IP locais da máquina host e classifica os pares de acordo com o qual o par de endereços é mais adequado para a comunicação entre os dois pares.</span><span class="sxs-lookup"><span data-stu-id="3f28c-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="3f28c-108">A função **CreateSortedAddressPairs** deve ser usada em vez do IOCTL de classificação da lista de endereços do **sio \_ \_ \_** no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3f28c-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="3f28c-109">As seções a seguir descrevem as considerações de uso para a **classificação da lista de endereços do sio \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="3f28c-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f28c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f28c-110">Parameters</span></span>

<span data-ttu-id="3f28c-111">O buffer passado para **a \_ \_ \_ classificação da lista de endereços sio** é uma estrutura de [**\_ \_ lista de endereços de soquete**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3f28c-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="3f28c-112">Cada [**\_ endereço de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) na lista deve estar no \_ formato SOCKADDR In6.</span><span class="sxs-lookup"><span data-stu-id="3f28c-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="3f28c-113">O IOCTL de classificação da lista de endereços do sio classifica os endereços IPv6 e IPv4 no Windows Vista e versões posteriores. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f28c-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="3f28c-114">Todos os endereços IPv4 na lista a serem classificados devem estar no formato de endereço IPv6 mapeado para IPv4.</span><span class="sxs-lookup"><span data-stu-id="3f28c-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="3f28c-115">Para obter mais informações sobre o formato de endereço IPv6 mapeado para IPv4, consulte [soquetes de pilha dupla](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="3f28c-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="3f28c-116">No Windows Server 2003 e no Windows XP, **a \_ \_ \_ classificação da lista de endereços do sio** classifica somente endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="3f28c-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="3f28c-117">Não há suporte para endereços IPv4 no formato de endereço IPv6 mapeados para IPv4.</span><span class="sxs-lookup"><span data-stu-id="3f28c-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="3f28c-118">Na saída, o membro **iAddressCount** da estrutura [**da \_ \_ lista de endereços de soquete**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) pode ser menor do que na entrada se o código do IOCTL determinar que alguns endereços de destino são inválidos.</span><span class="sxs-lookup"><span data-stu-id="3f28c-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="3f28c-119">Determinação da classificação</span><span class="sxs-lookup"><span data-stu-id="3f28c-119">Sorting Determination</span></span>

<span data-ttu-id="3f28c-120">A ordem de classificação para endereços IPv6 para a lista de endereços do SIO de \_ \_ classificação do \_ IOCTL é baseada na tabela de política de prefixo.</span><span class="sxs-lookup"><span data-stu-id="3f28c-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="3f28c-121">A tabela de diretivas de prefixo é configurada usando o utilitário de linha de comando *Netsh.exe* .</span><span class="sxs-lookup"><span data-stu-id="3f28c-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="3f28c-122">Os trechos de linha de comando a seguir ilustram os comandos básicos de configuração de tabela de prefixo de *Netsh.exe* :</span><span class="sxs-lookup"><span data-stu-id="3f28c-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="3f28c-123">No Windows Server 2003 e no Windows XP, o primeiro comando netsh listado acima foi o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3f28c-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="3f28c-124">Todos os outros comandos relacionados são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="3f28c-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="3f28c-125">A ordenação de endereço também é determinada por um algoritmo descrito no RFC 3484 na *seleção de endereço padrão para o IPv6 (protocolo IP versão 6)* publicado pela IETF.</span><span class="sxs-lookup"><span data-stu-id="3f28c-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="3f28c-126">Para obter mais informações, confira [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="3f28c-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="3f28c-127">(Este recurso só pode estar disponível em inglês.)</span><span class="sxs-lookup"><span data-stu-id="3f28c-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="3f28c-128">O **IOCTL \_ \_ \_ classificação da lista de endereços do sio** classifica os endereços do melhor para o pior e preenche os membros da **\_ \_ ID de escopo do sin6** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="3f28c-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="3f28c-129">Para endereços de site local, a lista de endereços SIOs é \_ \_ \_ preenchida ou elimina o endereço de escopo.</span><span class="sxs-lookup"><span data-stu-id="3f28c-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="3f28c-130">O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** ignora o endereço de origem associado ao soquete e classifica apenas pela lista de endereços de destino passada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3f28c-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="3f28c-131">A função [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) deve ser usada em vez do IOCTL de classificação da lista de endereços do **sio \_ \_ \_** no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3f28c-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="3f28c-132">A função **CreateSortedAddressPairs** retorna uma lista de pares de endereços que contém um endereço de origem local e um endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="3f28c-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="3f28c-133">Isso fornece um aplicativo o endereço de origem correto a ser usado para cada endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="3f28c-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="3f28c-134">Um aplicativo também pode filtrar os resultados procurando por um endereço de origem específico.</span><span class="sxs-lookup"><span data-stu-id="3f28c-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="3f28c-135">nos resultados.</span><span class="sxs-lookup"><span data-stu-id="3f28c-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f28c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f28c-136">Requirements</span></span>

<span data-ttu-id="3f28c-137">O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** é definido no arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="3f28c-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="3f28c-138">No SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o **sio de classificação da \_ \_ lista \_ de endereços** é definido no arquivo de cabeçalho *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="3f28c-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="3f28c-139">Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="3f28c-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="3f28c-140">O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** tem suporte no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3f28c-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f28c-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f28c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f28c-142">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="3f28c-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
