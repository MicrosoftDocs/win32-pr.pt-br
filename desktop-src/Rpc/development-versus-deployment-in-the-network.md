---
title: Desenvolvimento versus implantação na rede
description: A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005394"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="508cb-103">Desenvolvimento versus implantação na rede</span><span class="sxs-lookup"><span data-stu-id="508cb-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="508cb-104">A maioria dos desenvolvedores escreve e testa seus softwares em uma LAN confiável rápida.</span><span class="sxs-lookup"><span data-stu-id="508cb-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="508cb-105">O cliente e o servidor geralmente estão no mesmo segmento de rede.</span><span class="sxs-lookup"><span data-stu-id="508cb-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="508cb-106">Em tais circunstâncias, a rede raramente não responde e a conectividade raramente foi perdida.</span><span class="sxs-lookup"><span data-stu-id="508cb-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="508cb-107">No entanto, quando implantado em um ambiente de cliente, o cliente e o servidor geralmente estão em diferentes segmentos de rede, possivelmente geograficamente remotos, e o servidor é muito carregado com outros clientes.</span><span class="sxs-lookup"><span data-stu-id="508cb-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="508cb-108">Em outras palavras: não é possível supor a capacidade de resposta da rede.</span><span class="sxs-lookup"><span data-stu-id="508cb-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="508cb-109">Este artigo explica como construir arquiteturas robustas de cliente/servidor diante de incertezas introduzidas por uma rede intrinsecamente confiável e servidores potencialmente indisponíveis.</span><span class="sxs-lookup"><span data-stu-id="508cb-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




