---
title: Gerenciamento de contexto do provedor
description: Gerenciamento de contexto do provedor
ms.assetid: A73A6171-C81B-48EF-A689-3219E0B6B7C3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7970cdd6f3a69760a74ba4f0419ecb5022a339
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640742"
---
# <a name="provider-context-management"></a><span data-ttu-id="598f9-103">Gerenciamento de contexto do provedor</span><span class="sxs-lookup"><span data-stu-id="598f9-103">Provider Context Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="598f9-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="598f9-104">In this section</span></span>

-   [<span data-ttu-id="598f9-105">**\_CALLBACK0 de \_ alteração de contexto do provedor FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="598f9-105">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   [<span data-ttu-id="598f9-106">**FwpmProviderContextAdd0**</span><span class="sxs-lookup"><span data-stu-id="598f9-106">**FwpmProviderContextAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)
-   [<span data-ttu-id="598f9-107">**FwpmProviderContextAdd1**</span><span class="sxs-lookup"><span data-stu-id="598f9-107">**FwpmProviderContextAdd1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1)
-   [<span data-ttu-id="598f9-108">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="598f9-108">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="598f9-109">**FwpmProviderContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="598f9-109">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="598f9-110">**FwpmProviderContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="598f9-110">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="598f9-111">**FwpmProviderContextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="598f9-111">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="598f9-112">**FwpmProviderContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="598f9-112">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   [<span data-ttu-id="598f9-113">**FwpmProviderContextEnum0**</span><span class="sxs-lookup"><span data-stu-id="598f9-113">**FwpmProviderContextEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0)
-   [<span data-ttu-id="598f9-114">**FwpmProviderContextEnum1**</span><span class="sxs-lookup"><span data-stu-id="598f9-114">**FwpmProviderContextEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1)
-   [<span data-ttu-id="598f9-115">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="598f9-115">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="598f9-116">**FwpmProviderContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="598f9-116">**FwpmProviderContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0)
-   [<span data-ttu-id="598f9-117">**FwpmProviderContextGetById1**</span><span class="sxs-lookup"><span data-stu-id="598f9-117">**FwpmProviderContextGetById1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1)
-   [<span data-ttu-id="598f9-118">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="598f9-118">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="598f9-119">**FwpmProviderContextGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="598f9-119">**FwpmProviderContextGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0)
-   [<span data-ttu-id="598f9-120">**FwpmProviderContextGetByKey1**</span><span class="sxs-lookup"><span data-stu-id="598f9-120">**FwpmProviderContextGetByKey1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1)
-   [<span data-ttu-id="598f9-121">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="598f9-121">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="598f9-122">**FwpmProviderContextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="598f9-122">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="598f9-123">**FwpmProviderContextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="598f9-123">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="598f9-124">**FwpmProviderContextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="598f9-124">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="598f9-125">**FwpmProviderContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="598f9-125">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="598f9-126">**FwpmProviderContextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="598f9-126">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

 

 