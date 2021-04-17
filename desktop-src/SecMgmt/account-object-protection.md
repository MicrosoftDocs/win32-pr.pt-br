---
description: Explica como os objetos de conta são protegidos.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Proteção de objeto de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758267"
---
# <a name="account-object-protection"></a><span data-ttu-id="46e5b-103">Proteção de objeto de conta</span><span class="sxs-lookup"><span data-stu-id="46e5b-103">Account Object Protection</span></span>

<span data-ttu-id="46e5b-104">Os objetos de [**conta**](account-object.md) são protegidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="46e5b-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="46e5b-105">O **mundo** do grupo tem \_ execução genérica.</span><span class="sxs-lookup"><span data-stu-id="46e5b-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="46e5b-106">O **\_ administrador local** do grupo tem exclusão, \_ leitura genérica, \_ gravação genérica, \_ execução genérica e gravação de \_ acesso à DACL.</span><span class="sxs-lookup"><span data-stu-id="46e5b-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="46e5b-107">O **\_ administrador local** do grupo é atribuído como proprietário e grupo primário de objetos de conta.</span><span class="sxs-lookup"><span data-stu-id="46e5b-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



