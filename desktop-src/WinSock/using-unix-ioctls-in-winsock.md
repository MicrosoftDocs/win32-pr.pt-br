---
description: O comando SIOCGIFCONF fornecido pela maioria das implementações do UNIX tem suporte na forma de funções WSAIoctl e WSPIoctl com o comando SIO \_ obter a \_ lista de interface \_ . Esse comando retorna a lista de interfaces configuradas e seus parâmetros.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Usando os IOCTLs do UNIX no Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810729"
---
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="f460a-104">Usando os IOCTLs do UNIX no Winsock</span><span class="sxs-lookup"><span data-stu-id="f460a-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="f460a-105">O comando **SIOCGIFCONF** fornecido pela maioria das implementações do UNIX tem suporte na forma de funções [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) com o comando **sio obter a \_ \_ \_ lista de interface**.</span><span class="sxs-lookup"><span data-stu-id="f460a-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="f460a-106">Esse comando retorna a lista de interfaces configuradas e seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f460a-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="f460a-107">O suporte a esse comando é obrigatório para provedores de serviço TCP/IP em conformidade com o Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="f460a-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="f460a-108">O parâmetro *lpvOutBuffer* aponta para o buffer no qual [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) armazenam as informações sobre interfaces.</span><span class="sxs-lookup"><span data-stu-id="f460a-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="f460a-109">O número de interfaces (número de estruturas retornado em *lpvOutBuffer*) pode ser determinado com base no tamanho real do buffer de saída retornado em *lpcbBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="f460a-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 
