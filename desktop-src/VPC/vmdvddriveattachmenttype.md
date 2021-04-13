---
title: Enumeração VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Especifica o que está anexado a uma unidade de DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- VMDVDDriveAttachmentType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455372"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="7b57d-104">Enumeração VMDVDDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="7b57d-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="7b57d-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7b57d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7b57d-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7b57d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7b57d-107">Especifica o que está anexado a uma unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="7b57d-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b57d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b57d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="7b57d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="7b57d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7b57d-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="7b57d-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="7b57d-111">Não há nada anexado.</span><span class="sxs-lookup"><span data-stu-id="7b57d-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="7b57d-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**\_imagem vmDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="7b57d-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="7b57d-113">Há um arquivo de imagem ISO anexado.</span><span class="sxs-lookup"><span data-stu-id="7b57d-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="7b57d-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="7b57d-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="7b57d-115">Há uma unidade de CD ou DVD de host anexada.</span><span class="sxs-lookup"><span data-stu-id="7b57d-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b57d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b57d-116">Requirements</span></span>



| <span data-ttu-id="7b57d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b57d-117">Requirement</span></span> | <span data-ttu-id="7b57d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7b57d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b57d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b57d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b57d-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7b57d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b57d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b57d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b57d-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b57d-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7b57d-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7b57d-123">End of client support</span></span><br/>    | <span data-ttu-id="7b57d-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b57d-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7b57d-125">Produto</span><span class="sxs-lookup"><span data-stu-id="7b57d-125">Product</span></span><br/>                  | <span data-ttu-id="7b57d-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7b57d-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7b57d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b57d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b57d-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b57d-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b57d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b57d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b57d-130">**IVMDVDDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="7b57d-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

