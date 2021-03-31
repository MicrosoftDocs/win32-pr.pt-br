---
title: Informações de segurança e de erro estendidas
description: As informações de erro estendidas oferecem dados muito úteis ao solucionar um problema de RPC, mas esses dados muitas são considerados confidenciais por organizações preocupados com a segurança.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636919"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="ee678-103">Informações de segurança e de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="ee678-103">Security and Extended Error Information</span></span>

<span data-ttu-id="ee678-104">As informações de erro estendidas oferecem dados muito úteis ao solucionar um problema de RPC, mas esses dados muitas são considerados confidenciais por organizações preocupados com a segurança.</span><span class="sxs-lookup"><span data-stu-id="ee678-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="ee678-105">Em consideração sobre esses problemas de segurança, as informações de erro estendidas são desativadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="ee678-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="ee678-106">As informações de erro estendidas ainda são geradas quando as informações de erro estendidas são desabilitadas, mas as informações nunca são transmitidas entre os limites do processo ou do computador.</span><span class="sxs-lookup"><span data-stu-id="ee678-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="ee678-107">Essa abordagem permite que informações de erro sejam usadas por ferramentas que têm acesso ao espaço de endereço do processo, como os depuradores.</span><span class="sxs-lookup"><span data-stu-id="ee678-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="ee678-108">Quando ativado, as informações de erro estendidas são geradas e podem ser enviadas entre os limites do processo e do computador.</span><span class="sxs-lookup"><span data-stu-id="ee678-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="ee678-109">Atualmente, as informações de erro estendidas são usadas para sequências de protocolo orientadas por conexão e RPC local (LRPC).</span><span class="sxs-lookup"><span data-stu-id="ee678-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="ee678-110">Ele é parcialmente implementado para datagrams.</span><span class="sxs-lookup"><span data-stu-id="ee678-110">It is partially implemented for datagrams.</span></span>

 

 




