---
description: Tipos de partição válidos usados por drivers de disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipos de partição de disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756777"
---
# <a name="disk-partition-types"></a><span data-ttu-id="6305d-103">Tipos de partição de disco</span><span class="sxs-lookup"><span data-stu-id="6305d-103">Disk Partition Types</span></span>

<span data-ttu-id="6305d-104">A tabela a seguir identifica os tipos de partição válidos que são usados por drivers de disco.</span><span class="sxs-lookup"><span data-stu-id="6305d-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="6305d-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6305d-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="6305d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6305d-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="6305d-107"><dt>**Partição \_ do ENTRADA \_ não utilizada**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="6305d-108">Uma partição de entrada não utilizada.</span><span class="sxs-lookup"><span data-stu-id="6305d-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="6305d-109"><dt>**Partição \_ do 0x05 ESTENDIdo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6305d-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="6305d-110">Uma partição estendida.</span><span class="sxs-lookup"><span data-stu-id="6305d-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="6305d-111"><dt>**Partição \_ do FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="6305d-112">Uma partição do sistema de arquivos FAT12.</span><span class="sxs-lookup"><span data-stu-id="6305d-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="6305d-113"><dt>**Partição \_ do FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="6305d-114">Uma partição do sistema de arquivos FAT16.</span><span class="sxs-lookup"><span data-stu-id="6305d-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="6305d-115"><dt>**Partição \_ do**</dt> <dt>0X0B</dt> de FAT32</span><span class="sxs-lookup"><span data-stu-id="6305d-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="6305d-116">Uma partição do sistema de arquivos FAT32.</span><span class="sxs-lookup"><span data-stu-id="6305d-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="6305d-117"><dt>**Partição \_ do**</dt> <dt>0x07</dt> IFS</span><span class="sxs-lookup"><span data-stu-id="6305d-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="6305d-118">Uma partição IFS.</span><span class="sxs-lookup"><span data-stu-id="6305d-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="6305d-119"><dt>**Partição \_ do**</dt> <dt>0x42</dt> LDM</span><span class="sxs-lookup"><span data-stu-id="6305d-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="6305d-120">Uma partição LDM (Gerenciador de discos lógicos).</span><span class="sxs-lookup"><span data-stu-id="6305d-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="6305d-121"><dt>**Partição \_ do NTFT**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="6305d-122">Uma partição NTFT.</span><span class="sxs-lookup"><span data-stu-id="6305d-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="6305d-123"><dt>**Válido \_ NTFT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="6305d-124">Uma partição NTFT válida.</span><span class="sxs-lookup"><span data-stu-id="6305d-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="6305d-125">O alto bit de um código de tipo de partição indica que uma partição faz parte de um espelho NTFT ou uma matriz distribuída.</span><span class="sxs-lookup"><span data-stu-id="6305d-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6305d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="6305d-126">Remarks</span></span>

<span data-ttu-id="6305d-127">Há várias macros que podem ajudá-lo a detectar o tipo de partição: **IsContainerPartition**, **IsFTPartition** e **IsRecognizedPartition**.</span><span class="sxs-lookup"><span data-stu-id="6305d-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="6305d-128">Para obter mais informações, consulte WinIoCtl. h.</span><span class="sxs-lookup"><span data-stu-id="6305d-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="6305d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6305d-129">Requirements</span></span>



| <span data-ttu-id="6305d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6305d-130">Requirement</span></span> | <span data-ttu-id="6305d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6305d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6305d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6305d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6305d-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6305d-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6305d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6305d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6305d-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6305d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6305d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6305d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6305d-137"><dt>WinIoCtl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6305d-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6305d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6305d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6305d-139">**informações de partição \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="6305d-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="6305d-140">**informações de partição \_ \_ MBR**</span><span class="sxs-lookup"><span data-stu-id="6305d-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="6305d-141">**DEFINIR \_ informações de partição \_**</span><span class="sxs-lookup"><span data-stu-id="6305d-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




