---
description: Associa um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Classe AppDomainHelper (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500898"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="7ac95-103">Classe AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="7ac95-103">AppDomainHelper class</span></span>

<span data-ttu-id="7ac95-104">Associa um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.</span><span class="sxs-lookup"><span data-stu-id="7ac95-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="7ac95-105">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="7ac95-105">When to implement</span></span>

<span data-ttu-id="7ac95-106">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="7ac95-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="7ac95-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac95-107">Requirement</span></span> | <span data-ttu-id="7ac95-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7ac95-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="7ac95-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="7ac95-109">CLSID</span></span>      | <span data-ttu-id="7ac95-110">\_APPDOMAINHELPER GUID</span><span class="sxs-lookup"><span data-stu-id="7ac95-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="7ac95-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="7ac95-111">ProgID</span></span>     | <span data-ttu-id="7ac95-112">L "System. EnterpriseServices. Internal. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="7ac95-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="7ac95-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7ac95-113">Interfaces</span></span> | [<span data-ttu-id="7ac95-114">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="7ac95-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="7ac95-115">Quando usar</span><span class="sxs-lookup"><span data-stu-id="7ac95-115">When to use</span></span>

<span data-ttu-id="7ac95-116">Use essa classe para acessar os métodos de [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span><span class="sxs-lookup"><span data-stu-id="7ac95-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac95-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ac95-117">Remarks</span></span>

<span data-ttu-id="7ac95-118">Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7ac95-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="7ac95-119">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="7ac95-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="7ac95-120">Um objeto AppDomainHelper pode ser declarado usando "COMSVCSLib. AppDomainHelper" como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="7ac95-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac95-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ac95-121">Requirements</span></span>



| <span data-ttu-id="7ac95-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac95-122">Requirement</span></span> | <span data-ttu-id="7ac95-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ac95-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac95-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ac95-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac95-125">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="7ac95-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ac95-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ac95-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac95-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ac95-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ac95-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ac95-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac95-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac95-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac95-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ac95-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac95-131">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="7ac95-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

