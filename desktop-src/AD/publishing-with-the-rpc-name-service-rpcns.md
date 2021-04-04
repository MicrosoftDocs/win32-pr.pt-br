---
title: Publicando com o serviço de nome RPC
description: Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publicando com o serviço de nome RPC AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007300"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="4d279-104">Publicando com o serviço de nome RPC</span><span class="sxs-lookup"><span data-stu-id="4d279-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="4d279-105">Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="4d279-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="4d279-106">As APIs de RpcNs no Windows 2000 publicam as entradas RPC em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="4d279-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="4d279-107">Os serviços criam associações RPC e as publicam no namespace como entradas de servidor RPC nomeadas com atributos, incluindo a ID de interface exclusiva, um GUID reconhecido por clientes.</span><span class="sxs-lookup"><span data-stu-id="4d279-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="4d279-108">Um cliente pode então Pesquisar servidores RPC que ofereçam a interface desejada, importar a associação e conectar-se ao servidor.</span><span class="sxs-lookup"><span data-stu-id="4d279-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="4d279-109">Para obter mais informações sobre como publicar um serviço RPC, consulte [associação no lado do servidor](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="4d279-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 