---
title: Bluetooth e aceitar
description: O Bluetooth usa a função Accept para habilitar tentativas de conexão de entrada em um soquete.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- aceitar
- Bluetooth
- Bluetooth
- Bluetooth e aceitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749133"
---
# <a name="bluetooth-and-accept"></a><span data-ttu-id="9957c-107">Bluetooth e aceitar</span><span class="sxs-lookup"><span data-stu-id="9957c-107">Bluetooth and accept</span></span>

<span data-ttu-id="9957c-108">O Bluetooth usa a função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar tentativas de conexão de entrada em um soquete.</span><span class="sxs-lookup"><span data-stu-id="9957c-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="9957c-109">O \_ endereço de BTH do aplicativo cliente é obtido lendo a seção específica de transporte de Bluetooth da estrutura [**SOCKADDR**](/windows/desktop/WinSock/sockaddr-2) retornada.</span><span class="sxs-lookup"><span data-stu-id="9957c-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="9957c-110">O uso da função **Accept** com Bluetooth tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9957c-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="9957c-111">O parâmetro *addr* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um buffer que recebe o endereço da entidade de conexão, como conhecido pela camada de comunicação.</span><span class="sxs-lookup"><span data-stu-id="9957c-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="9957c-112">Um ponteiro para uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com o endereço de dispositivo Bluetooth remoto é retornado.</span><span class="sxs-lookup"><span data-stu-id="9957c-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="9957c-113">O parâmetro *addrlen* da função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) é um ponteiro opcional para um inteiro que contém o comprimento, em bytes, de addr. O inteiro deve ser maior ou igual ao valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span><span class="sxs-lookup"><span data-stu-id="9957c-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9957c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9957c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9957c-115">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9957c-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="9957c-116">**aceitar**</span><span class="sxs-lookup"><span data-stu-id="9957c-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 