---
description: Cria grupos de propriedades compartilhadas e obtém acesso a grupos de propriedades compartilhadas existentes.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Classe SharedPropertyGroupManager (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826318"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="23d95-103">Classe SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="23d95-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="23d95-104">Cria grupos de propriedades compartilhadas e obtém acesso a grupos de propriedades compartilhadas existentes.</span><span class="sxs-lookup"><span data-stu-id="23d95-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="23d95-105">Para obter mais informações sobre como usar o Gerenciador de Propriedades compartilhado no COM+, consulte [com+ Shared Gerenciador de propriedades](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="23d95-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="23d95-106">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="23d95-106">When to implement</span></span>

<span data-ttu-id="23d95-107">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="23d95-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="23d95-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="23d95-108">Requirement</span></span> | <span data-ttu-id="23d95-109">Valor</span><span class="sxs-lookup"><span data-stu-id="23d95-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="23d95-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="23d95-110">CLSID</span></span>      | <span data-ttu-id="23d95-111">\_SHAREDPROPERTYGROUPMANAGER CLSID</span><span class="sxs-lookup"><span data-stu-id="23d95-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="23d95-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="23d95-112">ProgID</span></span>     | <span data-ttu-id="23d95-113">L "MTxSpm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="23d95-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="23d95-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="23d95-114">Interfaces</span></span> | [<span data-ttu-id="23d95-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="23d95-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="23d95-116">Quando usar</span><span class="sxs-lookup"><span data-stu-id="23d95-116">When to use</span></span>

<span data-ttu-id="23d95-117">Use essa classe para acessar os métodos de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="23d95-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="23d95-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="23d95-118">Remarks</span></span>

<span data-ttu-id="23d95-119">Para criar esse objeto, chame [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="23d95-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="23d95-120">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="23d95-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="23d95-121">Um objeto SharedPropertyGroupManager pode ser declarado usando "COMSVCSLib. SharedPropertyGroupManager" como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="23d95-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d95-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23d95-122">Requirements</span></span>



| <span data-ttu-id="23d95-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="23d95-123">Requirement</span></span> | <span data-ttu-id="23d95-124">Valor</span><span class="sxs-lookup"><span data-stu-id="23d95-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23d95-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23d95-125">Minimum supported client</span></span><br/> | <span data-ttu-id="23d95-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23d95-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="23d95-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23d95-127">Minimum supported server</span></span><br/> | <span data-ttu-id="23d95-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23d95-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23d95-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23d95-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="23d95-130"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="23d95-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d95-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="23d95-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d95-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="23d95-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="23d95-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="23d95-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="23d95-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="23d95-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




