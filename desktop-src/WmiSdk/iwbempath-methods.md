---
description: A interface IWbemPath expõe os métodos a seguir.
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: Métodos IWbemPath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165326"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="b5f80-103">Métodos IWbemPath</span><span class="sxs-lookup"><span data-stu-id="b5f80-103">IWbemPath Methods</span></span>

<span data-ttu-id="b5f80-104">A interface [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5f80-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b5f80-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b5f80-105">In this section</span></span>

-   [<span data-ttu-id="b5f80-106">**Método CreateClassPart**</span><span class="sxs-lookup"><span data-stu-id="b5f80-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="b5f80-107">**Método DeleteClassPart**</span><span class="sxs-lookup"><span data-stu-id="b5f80-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="b5f80-108">**Método GetClassName**</span><span class="sxs-lookup"><span data-stu-id="b5f80-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="b5f80-109">**Método GetInfo**</span><span class="sxs-lookup"><span data-stu-id="b5f80-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="b5f80-110">**Método GetKeyList**</span><span class="sxs-lookup"><span data-stu-id="b5f80-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="b5f80-111">**Método GetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="b5f80-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="b5f80-112">**Método GetNamespaceCount**</span><span class="sxs-lookup"><span data-stu-id="b5f80-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="b5f80-113">**Método GetScope**</span><span class="sxs-lookup"><span data-stu-id="b5f80-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="b5f80-114">**Método GetScopeAsText**</span><span class="sxs-lookup"><span data-stu-id="b5f80-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="b5f80-115">**Método GetScopeCount**</span><span class="sxs-lookup"><span data-stu-id="b5f80-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="b5f80-116">**Método GetServer**</span><span class="sxs-lookup"><span data-stu-id="b5f80-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="b5f80-117">**Método GetText**</span><span class="sxs-lookup"><span data-stu-id="b5f80-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="b5f80-118">**Método IsLocal**</span><span class="sxs-lookup"><span data-stu-id="b5f80-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="b5f80-119">**Método isrelativo**</span><span class="sxs-lookup"><span data-stu-id="b5f80-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="b5f80-120">**Método IsRelativeOrChild**</span><span class="sxs-lookup"><span data-stu-id="b5f80-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="b5f80-121">**Método IsSameClassName**</span><span class="sxs-lookup"><span data-stu-id="b5f80-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="b5f80-122">**Método RemoveAllNamespaces**</span><span class="sxs-lookup"><span data-stu-id="b5f80-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="b5f80-123">**Método RemoveAllScopes**</span><span class="sxs-lookup"><span data-stu-id="b5f80-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="b5f80-124">**Método RemoveNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="b5f80-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="b5f80-125">**Método RemoveScope**</span><span class="sxs-lookup"><span data-stu-id="b5f80-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="b5f80-126">**Método setclassidname**</span><span class="sxs-lookup"><span data-stu-id="b5f80-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="b5f80-127">**Método SetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="b5f80-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="b5f80-128">**Método setscope**</span><span class="sxs-lookup"><span data-stu-id="b5f80-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="b5f80-129">**Método SetServer**</span><span class="sxs-lookup"><span data-stu-id="b5f80-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="b5f80-130">**Método SetText**</span><span class="sxs-lookup"><span data-stu-id="b5f80-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 



