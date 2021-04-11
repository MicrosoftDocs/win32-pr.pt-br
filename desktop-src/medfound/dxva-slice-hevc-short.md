---
description: Especifica dados de controle de fatia.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Estrutura de DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010311"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="05c66-103">\_Estrutura curta da fatia de DXVA \_ HEVC \_</span><span class="sxs-lookup"><span data-stu-id="05c66-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="05c66-104">Especifica dados de controle de fatia.</span><span class="sxs-lookup"><span data-stu-id="05c66-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05c66-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="05c66-106">Membros</span><span class="sxs-lookup"><span data-stu-id="05c66-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05c66-107">**BSNALunitDataLocation**</span><span class="sxs-lookup"><span data-stu-id="05c66-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="05c66-108">Especifica o local da unidade NAL.</span><span class="sxs-lookup"><span data-stu-id="05c66-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="05c66-109">**SliceBytesInBuffer**</span><span class="sxs-lookup"><span data-stu-id="05c66-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="05c66-110">O número de bytes no buffer de dados fragmentado que estão associados a essa estrutura de dados de controle de fatia.</span><span class="sxs-lookup"><span data-stu-id="05c66-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="05c66-111">**wBadSliceChopping**</span><span class="sxs-lookup"><span data-stu-id="05c66-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="05c66-112">Se a análise fragmentado fora do host for usada, esse valor indicará a fatia inadequada que está sendo desativada e conterá um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="05c66-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="05c66-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c66-113">Requirement</span></span> | <span data-ttu-id="05c66-114">Valor</span><span class="sxs-lookup"><span data-stu-id="05c66-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c66-115">Valor</span><span class="sxs-lookup"><span data-stu-id="05c66-115">Value</span></span> | <span data-ttu-id="05c66-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="05c66-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="05c66-117">0</span><span class="sxs-lookup"><span data-stu-id="05c66-117">0</span></span>     | <span data-ttu-id="05c66-118">Todos os bits da fatia estão localizados no buffer de dados fragmentado correspondente.</span><span class="sxs-lookup"><span data-stu-id="05c66-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="05c66-119">1</span><span class="sxs-lookup"><span data-stu-id="05c66-119">1</span></span>     | <span data-ttu-id="05c66-120">O buffer de dados fragmentado contém o início da fatia, mas não toda a fatia, porque o buffer está cheio.</span><span class="sxs-lookup"><span data-stu-id="05c66-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="05c66-121">2</span><span class="sxs-lookup"><span data-stu-id="05c66-121">2</span></span>     | <span data-ttu-id="05c66-122">O buffer de dados fragmentado contém o fim da fatia.</span><span class="sxs-lookup"><span data-stu-id="05c66-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="05c66-123">Ele não contém o início da fatia, pois o início da fatia estava localizado no buffer de dados fragmentado anterior.</span><span class="sxs-lookup"><span data-stu-id="05c66-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="05c66-124">3</span><span class="sxs-lookup"><span data-stu-id="05c66-124">3</span></span>     | <span data-ttu-id="05c66-125">O buffer de dados fragmentado não contém o início da fatia porque o início da fatia estava localizado no buffer de dados fragmentado anterior e não contém o final da fatia, pois o buffer de dados fragmentado atual também está cheio.</span><span class="sxs-lookup"><span data-stu-id="05c66-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05c66-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="05c66-126">Remarks</span></span>

<span data-ttu-id="05c66-127">**DXVA \_ Fatia \_ HEVC \_ Short** contém dados de controle de fatia que são passados para o acelerador de hardware do decodificador de software do host.</span><span class="sxs-lookup"><span data-stu-id="05c66-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c66-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c66-128">Requirements</span></span>



| <span data-ttu-id="05c66-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c66-129">Requirement</span></span> | <span data-ttu-id="05c66-130">Valor</span><span class="sxs-lookup"><span data-stu-id="05c66-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="05c66-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c66-131">Minimum supported client</span></span><br/> | <span data-ttu-id="05c66-132">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05c66-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="05c66-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c66-133">Minimum supported server</span></span><br/> | <span data-ttu-id="05c66-134">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="05c66-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="05c66-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05c66-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c66-136"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c66-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c66-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c66-138">Estruturas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05c66-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




