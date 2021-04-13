---
title: Enumeração VMFloppyDiskImageType (VPCCOMInterfaces. h)
description: Especifica os formatos de disquete.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- VMFloppyDiskImageType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369601"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="dd2d0-104">Enumeração VMFloppyDiskImageType</span><span class="sxs-lookup"><span data-stu-id="dd2d0-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="dd2d0-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd2d0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd2d0-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd2d0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd2d0-107">Especifica os formatos de disquete.</span><span class="sxs-lookup"><span data-stu-id="dd2d0-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2d0-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="dd2d0-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="dd2d0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd2d0-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-111">Formato desconhecido.</span><span class="sxs-lookup"><span data-stu-id="dd2d0-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage \_ LowDensity**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-113">Um 720K (formato de baixa densidade).</span><span class="sxs-lookup"><span data-stu-id="dd2d0-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage \_ Highdensity**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-115">Um formato de alta densidade (1,44 MB).</span><span class="sxs-lookup"><span data-stu-id="dd2d0-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**\_Dmf vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-117">Um formato de mídia de distribuição (1.68 MB).</span><span class="sxs-lookup"><span data-stu-id="dd2d0-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage \_ LowDensitySingleSided**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-119">Um formato de baixa densidade de um único lado.</span><span class="sxs-lookup"><span data-stu-id="dd2d0-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage \_ MediumDensity**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-121">Um formato de densidade média (1,2 MB).</span><span class="sxs-lookup"><span data-stu-id="dd2d0-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="dd2d0-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage \_ HighDensityMSS**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="dd2d0-123">Um MSS (tamanho de setor múltiplo) de alta densidade, usado pelo XDF (formato de distribuição estendido).</span><span class="sxs-lookup"><span data-stu-id="dd2d0-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2d0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd2d0-124">Requirements</span></span>



| <span data-ttu-id="dd2d0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd2d0-125">Requirement</span></span> | <span data-ttu-id="dd2d0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dd2d0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2d0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd2d0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2d0-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd2d0-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd2d0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd2d0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2d0-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dd2d0-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd2d0-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dd2d0-131">End of client support</span></span><br/>    | <span data-ttu-id="dd2d0-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd2d0-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd2d0-133">Produto</span><span class="sxs-lookup"><span data-stu-id="dd2d0-133">Product</span></span><br/>                  | <span data-ttu-id="dd2d0-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd2d0-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd2d0-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd2d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2d0-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2d0-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2d0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd2d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2d0-138">**IVMVirtualPC::CreateFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="dd2d0-139">**IVMVirtualPC::GetFloppyDiskImageType**</span><span class="sxs-lookup"><span data-stu-id="dd2d0-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

