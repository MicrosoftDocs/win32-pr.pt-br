---
description: A interface IWbemClassObject expõe os métodos a seguir.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: Métodos IWbemClassObject
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297666"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="0670d-103">Métodos IWbemClassObject</span><span class="sxs-lookup"><span data-stu-id="0670d-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="0670d-104">A interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0670d-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0670d-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0670d-105">In this section</span></span>

-   [<span data-ttu-id="0670d-106">**Método BeginEnumeration**</span><span class="sxs-lookup"><span data-stu-id="0670d-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="0670d-107">**Método BeginMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="0670d-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="0670d-108">**Método Clone**</span><span class="sxs-lookup"><span data-stu-id="0670d-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="0670d-109">**Método CompareTo**</span><span class="sxs-lookup"><span data-stu-id="0670d-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="0670d-110">**Método Delete**</span><span class="sxs-lookup"><span data-stu-id="0670d-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="0670d-111">**Método DeleteMethod**</span><span class="sxs-lookup"><span data-stu-id="0670d-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="0670d-112">**Método endenumeration**</span><span class="sxs-lookup"><span data-stu-id="0670d-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="0670d-113">**Método EndMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="0670d-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="0670d-114">**Método Get**</span><span class="sxs-lookup"><span data-stu-id="0670d-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="0670d-115">**Método GetMethod**</span><span class="sxs-lookup"><span data-stu-id="0670d-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="0670d-116">**Método GetMethodOrigin**</span><span class="sxs-lookup"><span data-stu-id="0670d-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="0670d-117">**Método GetMethodQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="0670d-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="0670d-118">**Método GetNames**</span><span class="sxs-lookup"><span data-stu-id="0670d-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="0670d-119">**Método GetObjectText**</span><span class="sxs-lookup"><span data-stu-id="0670d-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="0670d-120">**Método GetPropertyOrigin**</span><span class="sxs-lookup"><span data-stu-id="0670d-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="0670d-121">**Método GetPropertyQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="0670d-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="0670d-122">**Método getqualifierset**</span><span class="sxs-lookup"><span data-stu-id="0670d-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="0670d-123">**Método InheritsFrom**</span><span class="sxs-lookup"><span data-stu-id="0670d-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="0670d-124">**Próximo método**</span><span class="sxs-lookup"><span data-stu-id="0670d-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="0670d-125">**Método NextMethod**</span><span class="sxs-lookup"><span data-stu-id="0670d-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="0670d-126">**Método Put**</span><span class="sxs-lookup"><span data-stu-id="0670d-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="0670d-127">**Método PutMethod**</span><span class="sxs-lookup"><span data-stu-id="0670d-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="0670d-128">**Método SpawnDerivedClass**</span><span class="sxs-lookup"><span data-stu-id="0670d-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="0670d-129">**Método SpawnInstance**</span><span class="sxs-lookup"><span data-stu-id="0670d-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



