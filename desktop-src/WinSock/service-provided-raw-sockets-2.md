---
description: Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Soquetes brutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091308"
---
# <a name="raw-sockets"></a><span data-ttu-id="3c3c9-104">Soquetes brutos</span><span class="sxs-lookup"><span data-stu-id="3c3c9-104">Raw Sockets</span></span>

<span data-ttu-id="3c3c9-105">Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="3c3c9-106">O uso de soquetes brutos ao portar aplicativos para Winsock não é recomendado por vários motivos.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="3c3c9-107">A especificação do Windows Sockets não exige que um provedor de serviços Winsock dê suporte a soquetes brutos, ou seja, soquetes do tipo **Sock \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="3c3c9-108">No entanto, os provedores de serviços são incentivados a fornecer suporte a soquetes brutos.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="3c3c9-109">Um aplicativo compatível com Windows Sockets que deseja usar soquetes brutos deve tentar abrir o soquete com a chamada de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e, se ele falhar, tentar usar outro tipo de soquete ou indicar a falha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="3c3c9-110">No Windows 7, no Windows Server 2008 R2, no Windows Vista e no Windows XP com Service Pack 2 (SP2), a capacidade de enviar tráfego sobre soquetes brutos foi restrita de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="3c3c9-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="3c3c9-111">Para obter mais informações, consulte [soquetes brutos TCP/IP](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="3c3c9-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c3c9-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c3c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c3c9-113">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="3c3c9-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="3c3c9-114">**SSA**</span><span class="sxs-lookup"><span data-stu-id="3c3c9-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="3c3c9-115">Soquetes brutos TCP/IP</span><span class="sxs-lookup"><span data-stu-id="3c3c9-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="3c3c9-116">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="3c3c9-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



