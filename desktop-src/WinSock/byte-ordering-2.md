---
description: Sempre deve ser levado em consideração as diferenças entre a ordenação de bytes usada para armazenar inteiros pela arquitetura do host e a ordem de bytes usada na conexão por protocolos de transporte individuais.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordenação da regra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461118"
---
# <a name="byte-ordering"></a><span data-ttu-id="cc7c3-103">ordenação da regra</span><span class="sxs-lookup"><span data-stu-id="cc7c3-103">Byte Ordering</span></span>

<span data-ttu-id="cc7c3-104">Sempre deve ser levado em consideração as diferenças entre a ordenação de bytes usada para armazenar inteiros pela arquitetura do host e a ordem de bytes usada na conexão por protocolos de transporte individuais.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="cc7c3-105">Qualquer referência a um endereço ou número de porta passado para ou de uma rotina do Windows Sockets deve estar na ordem de rede (big-endian) para o protocolo que está sendo utilizado.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="cc7c3-106">No caso do IP, isso inclui o endereço IP e os parâmetros de porta de uma estrutura [**SOCKADDR**](sockaddr-2.md) (mas não o parâmetro *\_ da família Sin* ).</span><span class="sxs-lookup"><span data-stu-id="cc7c3-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="cc7c3-107">Vários sistemas UNIX operam em CPUs que representam inteiros em ordem de bytes de rede (big-endian).</span><span class="sxs-lookup"><span data-stu-id="cc7c3-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="cc7c3-108">Portanto, a necessidade de converter inteiros de ordem de bytes de host para ordem de bytes de rede pode ser ignorada sem causar problemas, mesmo que isso não seja recomendado para portabilidade.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="cc7c3-109">Por outro lado, a ordem de bytes usada para representar inteiros pela maioria das CPUs Intel® é little-endian.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="cc7c3-110">Portanto, se torna obrigatório que os inteiros sejam convertidos de ordem de byte de host para ordem de bytes de rede antes de serem usados em estruturas e funções de soquetes Winsock.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="cc7c3-111">Considere um aplicativo que normalmente entra em contato com um servidor na porta TCP correspondente ao serviço de tempo, mas fornece um mecanismo para que o usuário especifique uma porta alternativa.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="cc7c3-112">O número da porta retornado por [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) já está na ordem de rede, que é o formato necessário para construir um endereço para que nenhuma conversão seja necessária.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="cc7c3-113">No entanto, se o usuário optar por usar uma porta diferente, inserida como um inteiro, o aplicativo deverá convertê-la do host para a ordem de rede TCP/IP (usando a função [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) ou [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) antes de usá-la para construir um endereço.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="cc7c3-114">Por outro lado, se o aplicativo fosse exibir o número da porta dentro de um endereço (retornado por [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , por exemplo), o número da porta deve ser convertido da ordem da rede para o host (usando a função [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) ou [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) antes que possa ser exibido.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="cc7c3-115">Como as ordens de byte da Intel e da Internet são diferentes, as conversões descritas no anterior são inevitáveis.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="cc7c3-116">Os gravadores de aplicativo são cuidadosos de que devem usar as funções de conversão padrão fornecidas como parte do Winsock em vez de escrever seu próprio código de conversão, já que as implementações futuras do Winsock provavelmente serão executadas em sistemas para os quais a ordem de host é idêntica à ordem de bytes de rede.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="cc7c3-117">Somente os aplicativos que usam as funções de conversão padrão entre a ordem de bytes do host e da rede provavelmente serão portáteis.</span><span class="sxs-lookup"><span data-stu-id="cc7c3-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc7c3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc7c3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc7c3-119">**getemparelhaname**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="cc7c3-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="cc7c3-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="cc7c3-122">**htons**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="cc7c3-123">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="cc7c3-124">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="cc7c3-125">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="cc7c3-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="cc7c3-126">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="cc7c3-127">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="cc7c3-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="cc7c3-128">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="cc7c3-129">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="cc7c3-130">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="cc7c3-131">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="cc7c3-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



