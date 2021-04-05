---
description: Recupera informações sobre um assembly ao usar código gerenciado no Common Language Runtime de .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Classe ClrAssemblyLocator (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826269"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="f030a-103">Classe ClrAssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="f030a-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="f030a-104">Recupera informações sobre um assembly ao usar código gerenciado no Common Language Runtime de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f030a-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f030a-105">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="f030a-105">When to implement</span></span>

<span data-ttu-id="f030a-106">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="f030a-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f030a-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="f030a-107">Requirement</span></span> | <span data-ttu-id="f030a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f030a-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="f030a-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="f030a-109">CLSID</span></span>      | <span data-ttu-id="f030a-110">\_ASSEMBLYLOCATOR GUID</span><span class="sxs-lookup"><span data-stu-id="f030a-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="f030a-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="f030a-111">ProgID</span></span>     | <span data-ttu-id="f030a-112">L "System. EnterpriseServices. Internal. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="f030a-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="f030a-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f030a-113">Interfaces</span></span> | [<span data-ttu-id="f030a-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="f030a-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="f030a-115">Quando usar</span><span class="sxs-lookup"><span data-stu-id="f030a-115">When to use</span></span>

<span data-ttu-id="f030a-116">Use essa classe para acessar os métodos de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span><span class="sxs-lookup"><span data-stu-id="f030a-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="f030a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f030a-117">Remarks</span></span>

<span data-ttu-id="f030a-118">Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f030a-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="f030a-119">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="f030a-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="f030a-120">Um objeto ClrAssemblyLocator pode ser declarado usando "COMSVCSLib. ClrAssemblyLocator" como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="f030a-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f030a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f030a-121">Requirements</span></span>



| <span data-ttu-id="f030a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f030a-122">Requirement</span></span> | <span data-ttu-id="f030a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f030a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f030a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f030a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f030a-125">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="f030a-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f030a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f030a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f030a-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f030a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f030a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f030a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f030a-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f030a-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

