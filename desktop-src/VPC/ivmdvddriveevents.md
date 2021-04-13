---
title: Interface IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Virtual PC de interface IVMDVDDriveEvents
- Virtual PC de interface IVMDVDDriveEvents, descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455911"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="6cb28-105">Interface IVMDVDDriveEvents</span><span class="sxs-lookup"><span data-stu-id="6cb28-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="6cb28-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cb28-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6cb28-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6cb28-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6cb28-108">Define a interface de evento de saída para a interface [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="6cb28-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="6cb28-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6cb28-109">Members</span></span>

<span data-ttu-id="6cb28-110">A interface **IVMDVDDriveEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6cb28-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6cb28-111">**IVMDVDDriveEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6cb28-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="6cb28-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6cb28-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6cb28-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6cb28-113">Methods</span></span>

<span data-ttu-id="6cb28-114">A interface **IVMDVDDriveEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6cb28-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="6cb28-115">Método</span><span class="sxs-lookup"><span data-stu-id="6cb28-115">Method</span></span>                                                   | <span data-ttu-id="6cb28-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cb28-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="6cb28-117">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="6cb28-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="6cb28-118">Recebe a notificação de que a mídia foi ejetada da unidade.</span><span class="sxs-lookup"><span data-stu-id="6cb28-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="6cb28-119">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="6cb28-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="6cb28-120">Recebe a notificação de que a mídia foi inserida na unidade.</span><span class="sxs-lookup"><span data-stu-id="6cb28-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6cb28-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb28-121">Requirements</span></span>



| <span data-ttu-id="6cb28-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb28-122">Requirement</span></span> | <span data-ttu-id="6cb28-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb28-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb28-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb28-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6cb28-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cb28-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb28-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6cb28-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6cb28-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6cb28-128">End of client support</span></span><br/>    | <span data-ttu-id="6cb28-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6cb28-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6cb28-130">Produto</span><span class="sxs-lookup"><span data-stu-id="6cb28-130">Product</span></span><br/>                  | <span data-ttu-id="6cb28-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6cb28-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6cb28-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cb28-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb28-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb28-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6cb28-134">IID</span><span class="sxs-lookup"><span data-stu-id="6cb28-134">IID</span></span><br/>                      | <span data-ttu-id="6cb28-135">DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-E76C-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="6cb28-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

