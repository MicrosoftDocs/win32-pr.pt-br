---
description: A classe Provider expõe os métodos a seguir.
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: Métodos de provedor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811665"
---
# <a name="provider-methods"></a><span data-ttu-id="25c02-103">Métodos de provedor</span><span class="sxs-lookup"><span data-stu-id="25c02-103">Provider Methods</span></span>

<span data-ttu-id="25c02-104">\[A classe [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="25c02-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="25c02-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="25c02-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="25c02-106">A classe [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="25c02-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25c02-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="25c02-107">In this section</span></span>

-   [<span data-ttu-id="25c02-108">**Método Commit**</span><span class="sxs-lookup"><span data-stu-id="25c02-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="25c02-109">**Método CreateNewInstance**</span><span class="sxs-lookup"><span data-stu-id="25c02-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="25c02-110">[**Método DeleteInstance**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="25c02-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="25c02-111">**Método EnumerateInstances**</span><span class="sxs-lookup"><span data-stu-id="25c02-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="25c02-112">[**Método ExecMethod**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="25c02-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="25c02-113">**Método ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="25c02-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="25c02-114">**Método Flush**</span><span class="sxs-lookup"><span data-stu-id="25c02-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="25c02-115">**Método GetLocalComputerName**</span><span class="sxs-lookup"><span data-stu-id="25c02-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="25c02-116">**Método GetLocalInstancePath**</span><span class="sxs-lookup"><span data-stu-id="25c02-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="25c02-117">**Método GetNamespace**</span><span class="sxs-lookup"><span data-stu-id="25c02-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="25c02-118">[**Método GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="25c02-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="25c02-119">**Método GetProviderName**</span><span class="sxs-lookup"><span data-stu-id="25c02-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="25c02-120">**Método MakeLocalPath**</span><span class="sxs-lookup"><span data-stu-id="25c02-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="25c02-121">**Método de provedor**</span><span class="sxs-lookup"><span data-stu-id="25c02-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="25c02-122">[**Método PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="25c02-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="25c02-123">**Método SetCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="25c02-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="25c02-124">**Método ValidateDeletionFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="25c02-125">**Método ValidateEnumerationFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="25c02-126">**Método ValidateFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="25c02-127">**Método ValidateGetObjFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="25c02-128">**Método ValidateMethodFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="25c02-129">**Método ValidatePutInstanceFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="25c02-130">**Método ValidateQueryFlags**</span><span class="sxs-lookup"><span data-stu-id="25c02-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
