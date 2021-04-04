---
title: Enumeração VMDriveBusType (VPCCOMInterfaces. h)
description: Especifica o tipo de barramento.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- VMDriveBusType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085751"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="4bb5f-104">Enumeração VMDriveBusType</span><span class="sxs-lookup"><span data-stu-id="4bb5f-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="4bb5f-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4bb5f-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4bb5f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4bb5f-107">Especifica o tipo de barramento.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb5f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bb5f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="4bb5f-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="4bb5f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4bb5f-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="4bb5f-111">Nenhum tipo de barramento.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="4bb5f-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType \_ IDE**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="4bb5f-113">Tipo de barramento IDE.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="4bb5f-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType \_ SCSI**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="4bb5f-115">Tipo de barramento SCSI.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bb5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bb5f-116">Requirements</span></span>



| <span data-ttu-id="4bb5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb5f-117">Requirement</span></span> | <span data-ttu-id="4bb5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4bb5f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb5f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4bb5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb5f-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4bb5f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bb5f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4bb5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb5f-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4bb5f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4bb5f-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4bb5f-123">End of client support</span></span><br/>    | <span data-ttu-id="4bb5f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bb5f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4bb5f-125">Produto</span><span class="sxs-lookup"><span data-stu-id="4bb5f-125">Product</span></span><br/>                  | <span data-ttu-id="4bb5f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4bb5f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4bb5f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bb5f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bb5f-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb5f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

