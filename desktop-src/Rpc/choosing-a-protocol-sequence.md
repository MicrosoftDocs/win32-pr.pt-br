---
title: Escolhendo uma sequência de protocolo
description: As práticas recomendadas para escolher uma sequência de protocolo envolvem o uso de ncacn \_ IP \_ TCP e Ncalrpc, não ncacn \_ NP, ncacn \_ SPX e ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008081"
---
# <a name="choosing-a-protocol-sequence"></a><span data-ttu-id="6929a-103">Escolhendo uma sequência de protocolo</span><span class="sxs-lookup"><span data-stu-id="6929a-103">Choosing a Protocol Sequence</span></span>

<span data-ttu-id="6929a-104">**Prática recomendada:** Use [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) ao fazer uma chamada remota.</span><span class="sxs-lookup"><span data-stu-id="6929a-104">**Best practice:** Use [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) when making a remote call.</span></span> <span data-ttu-id="6929a-105">Use [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) para chamadas locais.</span><span class="sxs-lookup"><span data-stu-id="6929a-105">Use [**ncalrpc**](/windows/desktop/Midl/ncalrpc) for local calls.</span></span> <span data-ttu-id="6929a-106">Não use [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)ou qualquer uma das sequências de protocolo **ncadg \_ \*** ; elas são menos eficientes e têm recursos inferiores.</span><span class="sxs-lookup"><span data-stu-id="6929a-106">Do not use [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), [**ncacn\_spx**](/windows/desktop/Midl/ncacn-spx), or any of the **ncadg\_\*** protocol sequences; they are less efficient and have inferior capabilities.</span></span>

 

 