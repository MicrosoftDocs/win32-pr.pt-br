---
description: Em dois casos, era necessário renomear funções que são usadas em soquetes de Berkeley para evitar conflitos com outras funções da API do Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funções renomeadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827737"
---
# <a name="renamed-functions"></a><span data-ttu-id="e9136-103">Funções renomeadas</span><span class="sxs-lookup"><span data-stu-id="e9136-103">Renamed Functions</span></span>

<span data-ttu-id="e9136-104">Em dois casos, era necessário renomear funções que são usadas em soquetes de Berkeley para evitar conflitos com outras funções da API do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e9136-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="e9136-105">Fechar e fechamento</span><span class="sxs-lookup"><span data-stu-id="e9136-105">Close and Closesocket</span></span>

<span data-ttu-id="e9136-106">Os soquetes são representados por descritores de arquivo padrão em Berkeley Sockets, portanto, a função **Close** pode ser usada para fechar soquetes, bem como arquivos regulares.</span><span class="sxs-lookup"><span data-stu-id="e9136-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="e9136-107">Embora nada no Windows Sockets impeça uma implementação de usar identificadores de arquivo regulares para identificar soquetes, nada também exige isso.</span><span class="sxs-lookup"><span data-stu-id="e9136-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="e9136-108">No Windows, os soquetes devem ser fechados usando a rotina [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) .</span><span class="sxs-lookup"><span data-stu-id="e9136-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="e9136-109">NO Windows, o uso da função **Close** para fechar um soquete está incorreto e os efeitos dessa especificação são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="e9136-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="e9136-110">IOCTL e ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="e9136-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="e9136-111">Vários sistemas de tempo de execução de linguagem C usam os IOCTLs para fins não relacionados ao Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="e9136-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="e9136-112">Como consequência, a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) e a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) foram definidas para lidar com funções de soquete que foram executadas pelo **IOCTL** e pelo **fcntl** na distribuição de software Berkeley.</span><span class="sxs-lookup"><span data-stu-id="e9136-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9136-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9136-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9136-114">**fechamento**</span><span class="sxs-lookup"><span data-stu-id="e9136-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="e9136-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="e9136-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="e9136-116">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="e9136-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="e9136-117">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="e9136-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="e9136-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="e9136-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



