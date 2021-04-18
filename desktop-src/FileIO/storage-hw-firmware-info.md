---
description: Essa estrutura contém informações sobre o firmware do dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Estrutura de STORAGE_HW_FIRMWARE_INFO (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750863"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="0a940-103">\_Estrutura de \_ informações de firmware de hardware de armazenamento \_</span><span class="sxs-lookup"><span data-stu-id="0a940-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="0a940-104">Essa estrutura contém informações sobre o firmware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a940-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a940-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a940-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="0a940-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0a940-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a940-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="0a940-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-108">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="0a940-108">The version of this structure.</span></span> <span data-ttu-id="0a940-109">Isso deve ser definido como sizeof (informações de firmware de hardware de armazenamento \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="0a940-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="0a940-110">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="0a940-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-111">O tamanho dessa estrutura como um buffer, incluindo o slot.</span><span class="sxs-lookup"><span data-stu-id="0a940-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="0a940-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-113">Indica que este firmware dá suporte a uma atualização.</span><span class="sxs-lookup"><span data-stu-id="0a940-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="0a940-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0a940-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="0a940-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-117">O número de Slots de firmware no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a940-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="0a940-118">Esta é a dimensão da matriz de Slots.</span><span class="sxs-lookup"><span data-stu-id="0a940-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="0a940-119">Alguns dispositivos podem armazenar mais de 1 imagem de firmware, se tiverem mais de 1 slot de firmware.</span><span class="sxs-lookup"><span data-stu-id="0a940-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="0a940-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="0a940-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-121">O slot de firmware que contém a imagem de firmware ativa/em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0a940-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="0a940-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-123">O slot de firmware que está com a ativação pendente.</span><span class="sxs-lookup"><span data-stu-id="0a940-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="0a940-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-125">Indica que o firmware se aplica ao dispositivo e ao controlador/adaptador, por exemplo, SSD de NVMe.</span><span class="sxs-lookup"><span data-stu-id="0a940-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0a940-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0a940-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="0a940-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-129">O alinhamento da carga da imagem, em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="0a940-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="0a940-130">O máximo é o \_ tamanho da página.</span><span class="sxs-lookup"><span data-stu-id="0a940-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="0a940-131">O tamanho da transferência é um vários desse tamanho.</span><span class="sxs-lookup"><span data-stu-id="0a940-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="0a940-132">Alguns protocolos exigem pelo menos o tamanho do setor.</span><span class="sxs-lookup"><span data-stu-id="0a940-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="0a940-133">Quando esse valor é definido como 0, isso significa que esse valor é inválido.</span><span class="sxs-lookup"><span data-stu-id="0a940-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="0a940-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-135">O tamanho máximo da carga da imagem, que é usado para um único comando.</span><span class="sxs-lookup"><span data-stu-id="0a940-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="0a940-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="0a940-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="0a940-137">Contém as informações de slot para cada slot no dispositivo, do tipo [**\_ informações de \_ \_ slot \_ de firmware de HW de armazenamento**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="0a940-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a940-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a940-138">Requirements</span></span>



| <span data-ttu-id="0a940-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a940-139">Requirement</span></span> | <span data-ttu-id="0a940-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0a940-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a940-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a940-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0a940-142">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0a940-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="0a940-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a940-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0a940-144">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0a940-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="0a940-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a940-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a940-146"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a940-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a940-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a940-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a940-148">**\_ativação do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="0a940-149">**\_ativação do \_ firmware de HW de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="0a940-150">**\_download do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="0a940-151">**\_download de \_ firmware de hardware de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="0a940-152">**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="0a940-153">**\_consulta de \_ informações de firmware de hardware de armazenamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="0a940-154">**\_informações de \_ slot de firmware de hardware de armazenamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a940-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




