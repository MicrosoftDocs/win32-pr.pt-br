---
description: Quando um objeto TrustedDomain é criado, ele recebe uma proteção padrão.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Proteção de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779935"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="7b160-103">Proteção de objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="7b160-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="7b160-104">Quando um objeto [**TrustedDomain**](trusteddomain-object.md) é criado, ele recebe uma proteção padrão da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7b160-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="7b160-105">O grupo local mundial recebe acesso genérico de \_ execução.</span><span class="sxs-lookup"><span data-stu-id="7b160-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="7b160-106">O \_ grupo local de administração local recebe exclusão, \_ leitura genérica, \_ gravação genérica e acesso genérico de \_ execução.</span><span class="sxs-lookup"><span data-stu-id="7b160-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="7b160-107">O \_ grupo local de administração local é atribuído como proprietário e grupo primário do objeto.</span><span class="sxs-lookup"><span data-stu-id="7b160-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



