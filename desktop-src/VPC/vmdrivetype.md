---
title: Enumeração VMDriveType (VPCCOMInterfaces. h)
description: Especifica o tipo de unidade anexada a um local de barramento.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- VMDriveType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644624"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="ba2df-104">Enumeração VMDriveType</span><span class="sxs-lookup"><span data-stu-id="ba2df-104">VMDriveType enumeration</span></span>

<span data-ttu-id="ba2df-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ba2df-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba2df-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba2df-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba2df-107">Especifica o tipo de unidade anexada a um local de barramento.</span><span class="sxs-lookup"><span data-stu-id="ba2df-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba2df-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba2df-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="ba2df-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ba2df-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ba2df-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ nulo**</span><span class="sxs-lookup"><span data-stu-id="ba2df-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="ba2df-111">Não há unidade anexada.</span><span class="sxs-lookup"><span data-stu-id="ba2df-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="ba2df-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType \_ HD**</span><span class="sxs-lookup"><span data-stu-id="ba2df-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="ba2df-113">Há um disco rígido anexado.</span><span class="sxs-lookup"><span data-stu-id="ba2df-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="ba2df-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**\_DVD vmDriveType**</span><span class="sxs-lookup"><span data-stu-id="ba2df-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="ba2df-115">Há uma unidade de CD ou DVD anexada.</span><span class="sxs-lookup"><span data-stu-id="ba2df-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba2df-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba2df-116">Requirements</span></span>



| <span data-ttu-id="ba2df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba2df-117">Requirement</span></span> | <span data-ttu-id="ba2df-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ba2df-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba2df-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba2df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba2df-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba2df-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba2df-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba2df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba2df-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ba2df-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba2df-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ba2df-123">End of client support</span></span><br/>    | <span data-ttu-id="ba2df-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba2df-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba2df-125">Produto</span><span class="sxs-lookup"><span data-stu-id="ba2df-125">Product</span></span><br/>                  | <span data-ttu-id="ba2df-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba2df-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba2df-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba2df-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba2df-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba2df-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba2df-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba2df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba2df-130">**IVMVirtualMachine::AttachedDriveTypes**</span><span class="sxs-lookup"><span data-stu-id="ba2df-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

