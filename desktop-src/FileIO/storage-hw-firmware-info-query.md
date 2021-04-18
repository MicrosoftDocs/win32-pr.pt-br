---
description: Essa estrutura contém informações sobre o firmware do dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Estrutura de STORAGE_HW_FIRMWARE_INFO_QUERY (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782819"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="05d15-103">\_Estrutura de \_ consulta de informações de firmware de hardware de \_ armazenamento \_</span><span class="sxs-lookup"><span data-stu-id="05d15-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="05d15-104">Essa estrutura contém informações sobre o firmware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05d15-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05d15-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="05d15-106">Membros</span><span class="sxs-lookup"><span data-stu-id="05d15-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05d15-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="05d15-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="05d15-108">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="05d15-108">The version of this structure.</span></span> <span data-ttu-id="05d15-109">Isso deve ser definido como sizeof (consulta de informações de firmware de hardware de armazenamento \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="05d15-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="05d15-110">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="05d15-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="05d15-111">O tamanho dessa estrutura como um buffer.</span><span class="sxs-lookup"><span data-stu-id="05d15-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="05d15-112">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="05d15-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="05d15-113">Os sinalizadores associados à consulta.</span><span class="sxs-lookup"><span data-stu-id="05d15-113">The flags associated with the query.</span></span> <span data-ttu-id="05d15-114">Os seguintes são sinalizadores que podem ser definidos neste membro.</span><span class="sxs-lookup"><span data-stu-id="05d15-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="05d15-115">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="05d15-115">Flag</span></span>                                             | <span data-ttu-id="05d15-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="05d15-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05d15-117">\_controlador de \_ \_ sinalizador de solicitação de firmware HW \_ de \_ armazenamento</span><span class="sxs-lookup"><span data-stu-id="05d15-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="05d15-118">Indica que o destino da solicitação não é o próprio dispositivo ou o próprio objeto.</span><span class="sxs-lookup"><span data-stu-id="05d15-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="05d15-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="05d15-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="05d15-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="05d15-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05d15-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05d15-121">Requirements</span></span>



| <span data-ttu-id="05d15-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d15-122">Requirement</span></span> | <span data-ttu-id="05d15-123">Valor</span><span class="sxs-lookup"><span data-stu-id="05d15-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d15-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05d15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05d15-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="05d15-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="05d15-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05d15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05d15-127">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="05d15-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="05d15-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05d15-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d15-129"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05d15-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d15-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="05d15-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d15-131">**\_ativação do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="05d15-132">**\_ativação do \_ firmware de HW de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="05d15-133">**\_download do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="05d15-134">**\_download de \_ firmware de hardware de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="05d15-135">**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="05d15-136">**\_informações de \_ firmware de hardware de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="05d15-137">**\_informações de \_ slot de firmware de hardware de armazenamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05d15-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




