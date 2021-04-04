---
description: Descreve como o objeto de política é protegido por padrão.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Proteção de objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646997"
---
# <a name="policy-object-protection"></a><span data-ttu-id="76869-103">Proteção de objeto de política</span><span class="sxs-lookup"><span data-stu-id="76869-103">Policy Object Protection</span></span>

<span data-ttu-id="76869-104">O objeto de [**política**](policy-object.md) é protegido por padrão com as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="76869-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="76869-105">O mundo do grupo local tem \_ acesso genérico de execução.</span><span class="sxs-lookup"><span data-stu-id="76869-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="76869-106">O sistema de ID conhecido recebe \_ todos os \_ acessos à política.</span><span class="sxs-lookup"><span data-stu-id="76869-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="76869-107">O administrador LOCAL do grupo local \_ tem \_ acesso genérico de leitura, \_ gravação genérica e \_ execução genérica.</span><span class="sxs-lookup"><span data-stu-id="76869-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="76869-108">O administrador LOCAL do grupo \_ é atribuído como proprietário e grupo primário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="76869-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="76869-109">O objeto de [**política**](policy-object.md) não pode ser criado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="76869-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



