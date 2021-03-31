---
title: Enumeração vmFloppyDriveEvent (VPCCOMInterfaces. h)
description: Especifica os eventos da unidade de disquete.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- vmFloppyDriveEvent de enumeração Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645044"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="7312d-104">Enumeração vmFloppyDriveEvent</span><span class="sxs-lookup"><span data-stu-id="7312d-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="7312d-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7312d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7312d-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7312d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7312d-107">Especifica os eventos da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="7312d-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7312d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7312d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="7312d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="7312d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7312d-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="7312d-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="7312d-111">Uma imagem de disquete é anexada ou a mídia real é inserida em uma unidade de host.</span><span class="sxs-lookup"><span data-stu-id="7312d-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="7312d-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ Onejeção**</span><span class="sxs-lookup"><span data-stu-id="7312d-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="7312d-113">A mídia foi ejetada.</span><span class="sxs-lookup"><span data-stu-id="7312d-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7312d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7312d-114">Requirements</span></span>



| <span data-ttu-id="7312d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7312d-115">Requirement</span></span> | <span data-ttu-id="7312d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7312d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7312d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7312d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7312d-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7312d-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7312d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7312d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7312d-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7312d-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7312d-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7312d-121">End of client support</span></span><br/>    | <span data-ttu-id="7312d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7312d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7312d-123">Produto</span><span class="sxs-lookup"><span data-stu-id="7312d-123">Product</span></span><br/>                  | <span data-ttu-id="7312d-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7312d-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7312d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7312d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7312d-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7312d-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7312d-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7312d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7312d-128">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="7312d-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

