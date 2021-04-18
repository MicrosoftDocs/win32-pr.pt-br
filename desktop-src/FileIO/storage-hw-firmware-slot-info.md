---
description: Essa estrutura contém informações sobre um slot em um dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Estrutura de STORAGE_HW_FIRMWARE_SLOT_INFO (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767654"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="a4c1d-103">\_Estrutura de \_ informações do slot do firmware de hardware de \_ armazenamento \_</span><span class="sxs-lookup"><span data-stu-id="a4c1d-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="a4c1d-104">Essa estrutura contém informações sobre um slot em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c1d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4c1d-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="a4c1d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a4c1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4c1d-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-108">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-108">The version of this structure.</span></span> <span data-ttu-id="a4c1d-109">Isso deve ser definido como sizeof (informações de slot de firmware de hardware de armazenamento \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="a4c1d-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-110">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-111">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-113">O número do slot deste slot.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-114">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-115">Indica se este slot é somente leitura ou não.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-117">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1d-120">**Revisão**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="a4c1d-121">A revisão do firmware neste slot.</span><span class="sxs-lookup"><span data-stu-id="a4c1d-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4c1d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c1d-122">Requirements</span></span>



| <span data-ttu-id="a4c1d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c1d-123">Requirement</span></span> | <span data-ttu-id="a4c1d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c1d-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c1d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c1d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c1d-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a4c1d-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="a4c1d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c1d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c1d-128">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a4c1d-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="a4c1d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4c1d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c1d-130"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4c1d-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c1d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4c1d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c1d-132">**\_ativação do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a4c1d-133">**\_ativação do \_ firmware de HW de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a4c1d-134">**\_download do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="a4c1d-135">**\_download de \_ firmware de hardware de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="a4c1d-136">**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="a4c1d-137">**\_informações de \_ firmware de hardware de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="a4c1d-138">**\_consulta de \_ informações de firmware de hardware de armazenamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4c1d-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




