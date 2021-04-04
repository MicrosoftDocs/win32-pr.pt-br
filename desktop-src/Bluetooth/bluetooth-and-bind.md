---
title: Bluetooth e ligar
description: O Bluetooth usa a função de associação para associar a um soquete.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth e ligar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823961"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="ea639-107">Bluetooth e ligar</span><span class="sxs-lookup"><span data-stu-id="ea639-107">Bluetooth and bind</span></span>

<span data-ttu-id="ea639-108">O Bluetooth usa a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) para associar a um soquete.</span><span class="sxs-lookup"><span data-stu-id="ea639-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="ea639-109">Para associar um soquete Bluetooth, chame a função **BIND** usando a estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) .</span><span class="sxs-lookup"><span data-stu-id="ea639-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="ea639-110">Use a estrutura **SOCKADDR \_ BTH** com as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ea639-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="ea639-111">Em aplicativos cliente, o membro da porta deve ser zero para permitir que um ponto de extremidade local apropriado seja atribuído.</span><span class="sxs-lookup"><span data-stu-id="ea639-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="ea639-112">Em aplicativos de servidor, o membro de porta deve ser um número de porta ou uma porta BT válida \_ \_ ; portas atribuídas automaticamente usando \_ a porta BT \_ podem ser consultadas subsequentemente com uma chamada para a função [**getsockname**](bluetooth-and-getsockname.md) .</span><span class="sxs-lookup"><span data-stu-id="ea639-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="ea639-113">O intervalo válido para solicitar uma porta RFCOMM específica é de 1 a 30.</span><span class="sxs-lookup"><span data-stu-id="ea639-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="ea639-114">Os canais de servidor são recursos globais e apenas 30 canais de servidor estão disponíveis para RFCOMM em qualquer dispositivo Bluetooth, que deve ser compartilhado por todos os soquetes do Windows que pertencem à família de endereços Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ea639-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="ea639-115">Se nenhum canal de servidor estiver disponível ou se o canal de servidor especificado já estiver reservado, a chamada de [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.</span><span class="sxs-lookup"><span data-stu-id="ea639-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="ea639-116">Após o retorno bem-sucedido da associação, o canal do servidor será reservado até que o soquete seja fechado.</span><span class="sxs-lookup"><span data-stu-id="ea639-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="ea639-117">Use a função [**getsockname**](bluetooth-and-getsockname.md) para recuperar o número de canal para o registro de SDP.</span><span class="sxs-lookup"><span data-stu-id="ea639-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="ea639-118">Os aplicativos devem usar a alocação automática para o canal do servidor.</span><span class="sxs-lookup"><span data-stu-id="ea639-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="ea639-119">A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) não anuncia automaticamente o aplicativo de servidor usando o Bluetooth SDP; os aplicativos devem chamar a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para serem encontrados por aplicativos Bluetooth remotos.</span><span class="sxs-lookup"><span data-stu-id="ea639-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea639-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea639-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea639-121">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ea639-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="ea639-122">**associa**</span><span class="sxs-lookup"><span data-stu-id="ea639-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 