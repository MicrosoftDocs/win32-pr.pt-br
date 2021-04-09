---
description: A função socket criou soquetes com o atributo Overlapped definido por padrão na primeira Wsock32.dll, a versão de 32 bits do Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Estado padrão para o atributo sobreposto de um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090398"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="194b8-103">Estado padrão para o atributo sobreposto de um soquete</span><span class="sxs-lookup"><span data-stu-id="194b8-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="194b8-104">A função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) criou soquetes com o atributo Overlapped definido por padrão na primeira Wsock32.dll, a versão de 32 bits do Windows sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="194b8-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="194b8-105">Para garantir a compatibilidade com versões anteriores atualmente implantadas Wsock32.dll, isso continuará sendo o caso do Windows Sockets 2 também.</span><span class="sxs-lookup"><span data-stu-id="194b8-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="194b8-106">Ou seja, nos soquetes do Windows Sockets 2 criados com a função **Socket** terão o atributo Overlapped.</span><span class="sxs-lookup"><span data-stu-id="194b8-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="194b8-107">No entanto, para ser mais compatível com o restante da API do Windows, os soquetes criados com [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) não serão, por padrão, o atributo sobreposto.</span><span class="sxs-lookup"><span data-stu-id="194b8-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="194b8-108">Esse atributo só será aplicado se o \_ bit sobreposto do sinalizador WSA \_ estiver definido.</span><span class="sxs-lookup"><span data-stu-id="194b8-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



