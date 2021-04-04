---
title: Florestas
description: Uma floresta é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Active Directory de florestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917128"
---
# <a name="forests"></a><span data-ttu-id="47f73-104">Florestas</span><span class="sxs-lookup"><span data-stu-id="47f73-104">Forests</span></span>

<span data-ttu-id="47f73-105">Uma [*floresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo.</span><span class="sxs-lookup"><span data-stu-id="47f73-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="47f73-106">Todas as árvores em uma floresta compartilham um esquema, uma configuração e um catálogo global comuns.</span><span class="sxs-lookup"><span data-stu-id="47f73-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="47f73-107">Todas as árvores em uma determinada floresta de confiança do Exchange de acordo com relações de confiança Kerberos hierárquicas transitivas.</span><span class="sxs-lookup"><span data-stu-id="47f73-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="47f73-108">Ao contrário das árvores, uma floresta não requer um nome distinto.</span><span class="sxs-lookup"><span data-stu-id="47f73-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="47f73-109">Existe uma floresta como um conjunto de objetos de referência cruzada e relações de confiança Kerberos reconhecidas pelas árvores de membros.</span><span class="sxs-lookup"><span data-stu-id="47f73-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="47f73-110">As árvores em uma floresta formam uma hierarquia para fins de confiança Kerberos; o nome da árvore na raiz da árvore de confiança refere-se a uma determinada floresta.</span><span class="sxs-lookup"><span data-stu-id="47f73-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="47f73-111">A figura a seguir mostra uma floresta de namespaces não contíguos.</span><span class="sxs-lookup"><span data-stu-id="47f73-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![floresta de namespaces não contíguos](images/forests.png)

 

 