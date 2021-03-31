---
title: Enumeração VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Especifica os eventos da unidade de DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- VMDVDDriveEvent de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644623"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="7c4a8-104">Enumeração VMDVDDriveEvent</span><span class="sxs-lookup"><span data-stu-id="7c4a8-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="7c4a8-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7c4a8-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7c4a8-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7c4a8-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7c4a8-107">Especifica os eventos da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="7c4a8-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c4a8-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="7c4a8-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="7c4a8-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7c4a8-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="7c4a8-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="7c4a8-111">Uma imagem ISO é anexada ou a mídia real é inserida em uma unidade do host.</span><span class="sxs-lookup"><span data-stu-id="7c4a8-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="7c4a8-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ Onejeção**</span><span class="sxs-lookup"><span data-stu-id="7c4a8-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="7c4a8-113">A mídia foi ejetada.</span><span class="sxs-lookup"><span data-stu-id="7c4a8-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c4a8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c4a8-114">Requirements</span></span>



| <span data-ttu-id="7c4a8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4a8-115">Requirement</span></span> | <span data-ttu-id="7c4a8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7c4a8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4a8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c4a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4a8-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7c4a8-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c4a8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c4a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4a8-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7c4a8-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7c4a8-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7c4a8-121">End of client support</span></span><br/>    | <span data-ttu-id="7c4a8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c4a8-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7c4a8-123">Produto</span><span class="sxs-lookup"><span data-stu-id="7c4a8-123">Product</span></span><br/>                  | <span data-ttu-id="7c4a8-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7c4a8-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7c4a8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c4a8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4a8-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4a8-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4a8-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7c4a8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4a8-128">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="7c4a8-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

