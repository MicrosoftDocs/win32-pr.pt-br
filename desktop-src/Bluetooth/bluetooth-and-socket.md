---
title: Bluetooth e soquete
description: Cria um soquete para conexões de entrada ou saída.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth de Bluetooth
- soquete Bluetooth
- Bluetooth e soquete Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641187"
---
# <a name="bluetooth-and-socket"></a><span data-ttu-id="209de-106">Bluetooth e soquete</span><span class="sxs-lookup"><span data-stu-id="209de-106">Bluetooth and socket</span></span>

<span data-ttu-id="209de-107">A função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) cria um soquete para conexões de entrada ou saída.:</span><span class="sxs-lookup"><span data-stu-id="209de-107">The [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function creates a socket for incoming or outgoing connections.:</span></span>

<span data-ttu-id="209de-108">Para criar um soquete usando Bluetooth, use as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="209de-108">To create a socket using Bluetooth, use the following settings:</span></span>

-   <span data-ttu-id="209de-109">O parâmetro *AF* da função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) é sempre definido como **AF \_ BTH** para soquetes Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="209de-109">The *af* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always set to **AF\_BTH** for Bluetooth sockets.</span></span>
-   <span data-ttu-id="209de-110">O parâmetro de *tipo* da função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) é sempre **Sock \_ Stream**; **Sock \_** Os soquetes DGRAM não têm suporte do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="209de-110">The *type* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always **SOCK\_STREAM**; **SOCK\_DGRAM** sockets are not supported by Bluetooth.</span></span>
-   <span data-ttu-id="209de-111">Para o parâmetro de *protocolo* , **BTHPROTO \_ RFCOMM** é o protocolo com suporte.</span><span class="sxs-lookup"><span data-stu-id="209de-111">For the *protocol* parameter, **BTHPROTO\_RFCOMM** is the supported protocol.</span></span>

<span data-ttu-id="209de-112">Para obter mais informações, consulte [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span><span class="sxs-lookup"><span data-stu-id="209de-112">For more information, see [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="209de-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="209de-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209de-114">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="209de-114">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="209de-115">**SSA**</span><span class="sxs-lookup"><span data-stu-id="209de-115">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 