---
description: O Windows Sockets 2 não pressupõe que a ordem de bytes de rede para todos os protocolos seja a mesma.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rotinas de conversão de Byte-Order estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501699"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="0f45d-103">Rotinas de conversão de Byte-Order estendidas</span><span class="sxs-lookup"><span data-stu-id="0f45d-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="0f45d-104">O Windows Sockets 2 não pressupõe que a ordem de bytes de rede para todos os protocolos seja a mesma.</span><span class="sxs-lookup"><span data-stu-id="0f45d-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="0f45d-105">Um conjunto de rotinas de conversão é fornecido para a conversão de quantidades de 16 bits e de 32 bits de e para a ordem de bytes da rede.</span><span class="sxs-lookup"><span data-stu-id="0f45d-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="0f45d-106">Essas rotinas assumem como um parâmetro de entrada o identificador de soquete que tem uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associada a ela.</span><span class="sxs-lookup"><span data-stu-id="0f45d-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="0f45d-107">O membro **NetworkByteOrder** da estrutura **de \_ informações de WSAPROTOCOL** especifica a ordem de bytes de rede desejada (atualmente big-endian ou little-endian).</span><span class="sxs-lookup"><span data-stu-id="0f45d-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f45d-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f45d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f45d-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="0f45d-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="0f45d-110">**htons**</span><span class="sxs-lookup"><span data-stu-id="0f45d-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="0f45d-111">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="0f45d-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="0f45d-112">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="0f45d-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="0f45d-113">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="0f45d-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="0f45d-114">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="0f45d-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="0f45d-115">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="0f45d-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="0f45d-116">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="0f45d-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="0f45d-117">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="0f45d-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="0f45d-118">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="0f45d-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="0f45d-119">**informações de WSAPROTOCOL \_**</span><span class="sxs-lookup"><span data-stu-id="0f45d-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
