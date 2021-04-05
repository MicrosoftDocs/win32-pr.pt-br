---
title: Enumeração VMFloppyDriveAttachmentType (VPCCOMInterfaces. h)
description: Especifica o que está anexado a uma unidade de disquete.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- VMFloppyDriveAttachmentType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918639"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="89d83-104">Enumeração VMFloppyDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="89d83-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="89d83-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89d83-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89d83-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89d83-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89d83-107">Especifica o que está anexado a uma unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="89d83-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89d83-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="89d83-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="89d83-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="89d83-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="89d83-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="89d83-111">Não há nada anexado.</span><span class="sxs-lookup"><span data-stu-id="89d83-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="89d83-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**\_imagem vmFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="89d83-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="89d83-113">Há um arquivo de imagem de disquete anexado.</span><span class="sxs-lookup"><span data-stu-id="89d83-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="89d83-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="89d83-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="89d83-115">Há uma unidade de disquete de host conectada.</span><span class="sxs-lookup"><span data-stu-id="89d83-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89d83-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d83-116">Requirements</span></span>



| <span data-ttu-id="89d83-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d83-117">Requirement</span></span> | <span data-ttu-id="89d83-118">Valor</span><span class="sxs-lookup"><span data-stu-id="89d83-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d83-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d83-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89d83-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="89d83-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89d83-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d83-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89d83-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="89d83-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89d83-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="89d83-123">End of client support</span></span><br/>    | <span data-ttu-id="89d83-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89d83-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89d83-125">Produto</span><span class="sxs-lookup"><span data-stu-id="89d83-125">Product</span></span><br/>                  | <span data-ttu-id="89d83-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89d83-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89d83-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89d83-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="89d83-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d83-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d83-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="89d83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d83-130">**IVMFloppyDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="89d83-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

