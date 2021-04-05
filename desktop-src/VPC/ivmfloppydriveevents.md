---
title: Interface IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMFloppyDrive. O cliente implementa esses métodos para receber eventos enviados do IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Virtual PC de interface IVMFloppyDriveEvents
- Virtual PC de interface IVMFloppyDriveEvents, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086349"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="d799f-106">Interface IVMFloppyDriveEvents</span><span class="sxs-lookup"><span data-stu-id="d799f-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="d799f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d799f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d799f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d799f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d799f-109">Define a interface de evento de saída para a interface [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="d799f-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="d799f-110">O cliente implementa esses métodos para receber eventos enviados do **IVMFloppyDrive**.</span><span class="sxs-lookup"><span data-stu-id="d799f-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="d799f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d799f-111">Members</span></span>

<span data-ttu-id="d799f-112">A interface **IVMFloppyDriveEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d799f-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d799f-113">**IVMFloppyDriveEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d799f-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="d799f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d799f-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d799f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="d799f-115">Methods</span></span>

<span data-ttu-id="d799f-116">A interface **IVMFloppyDriveEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d799f-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="d799f-117">Método</span><span class="sxs-lookup"><span data-stu-id="d799f-117">Method</span></span>                                                      | <span data-ttu-id="d799f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d799f-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="d799f-119">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="d799f-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="d799f-120">Recebe a notificação de que a mídia foi ejetada da unidade.</span><span class="sxs-lookup"><span data-stu-id="d799f-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="d799f-121">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="d799f-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="d799f-122">Recebe a notificação de que a mídia foi inserida na unidade.</span><span class="sxs-lookup"><span data-stu-id="d799f-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d799f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d799f-123">Requirements</span></span>



| <span data-ttu-id="d799f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d799f-124">Requirement</span></span> | <span data-ttu-id="d799f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d799f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d799f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d799f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d799f-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d799f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d799f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d799f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d799f-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d799f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d799f-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d799f-130">End of client support</span></span><br/>    | <span data-ttu-id="d799f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d799f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d799f-132">Produto</span><span class="sxs-lookup"><span data-stu-id="d799f-132">Product</span></span><br/>                  | <span data-ttu-id="d799f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d799f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d799f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d799f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d799f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d799f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d799f-136">IID</span><span class="sxs-lookup"><span data-stu-id="d799f-136">IID</span></span><br/>                      | <span data-ttu-id="d799f-137">DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="d799f-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

