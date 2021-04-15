---
title: Acessando ponteiros opacos
description: Os clientes são capazes de acessar as informações armazenadas em destinos usando ponteiros opacos.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498740"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="0cbdc-103">Acessando ponteiros opacos</span><span class="sxs-lookup"><span data-stu-id="0cbdc-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="0cbdc-104">Os clientes são capazes de acessar as informações armazenadas em destinos usando ponteiros opacos.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="0cbdc-105">Para usar o armazenamento, o cliente deve primeiro chamar [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obter o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="0cbdc-106">Sempre que uma alteração nas informações é necessária, o cliente deve primeiro bloquear o destino chamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) com o parâmetro *LockDest* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="0cbdc-107">Depois que o destino estiver bloqueado, o cliente poderá fazer a alteração necessária.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="0cbdc-108">O destino pode ser desbloqueado usando outra chamada para **RtmLockDestination** com o parâmetro *LockDest* definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="0cbdc-109">A função [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) também permite que um cliente use um bloqueio de leitura ou um bloqueio de gravação, usando o parâmetro *exclusivo* .</span><span class="sxs-lookup"><span data-stu-id="0cbdc-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="0cbdc-110">Um cliente deve usar o bloqueio de gravação somente quando estiver fazendo alterações nas informações mantidas usando o ponteiro opaco.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="0cbdc-111">Os clientes podem usar o bloqueio de leitura para exibir as informações de ponteiro opacos armazenadas em um destino.</span><span class="sxs-lookup"><span data-stu-id="0cbdc-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="0cbdc-112">Para obter um exemplo de código que mostra como usar essas funções, consulte [acessar o ponteiro opaco em um destino](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="0cbdc-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




