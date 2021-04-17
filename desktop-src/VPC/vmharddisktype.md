---
title: Enumeração VMHardDiskType (VPCCOMInterfaces. h)
description: Especifica o tipo de imagem do disco rígido.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- VMHardDiskType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770579"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="c689e-104">Enumeração VMHardDiskType</span><span class="sxs-lookup"><span data-stu-id="c689e-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="c689e-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c689e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c689e-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c689e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c689e-107">Especifica o tipo de imagem do disco rígido.</span><span class="sxs-lookup"><span data-stu-id="c689e-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c689e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c689e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="c689e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="c689e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c689e-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ dinâmico**</span><span class="sxs-lookup"><span data-stu-id="c689e-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="c689e-111">Uma imagem de disco rígido de expansão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c689e-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="c689e-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="c689e-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="c689e-113">Uma imagem de disco rígido de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="c689e-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="c689e-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**\_diferenciação de vmDiskType**</span><span class="sxs-lookup"><span data-stu-id="c689e-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="c689e-115">Uma imagem de disco rígido diferencial.</span><span class="sxs-lookup"><span data-stu-id="c689e-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c689e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c689e-116">Requirements</span></span>



| <span data-ttu-id="c689e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c689e-117">Requirement</span></span> | <span data-ttu-id="c689e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c689e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c689e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c689e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c689e-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c689e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c689e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c689e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c689e-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c689e-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c689e-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c689e-123">End of client support</span></span><br/>    | <span data-ttu-id="c689e-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c689e-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c689e-125">Produto</span><span class="sxs-lookup"><span data-stu-id="c689e-125">Product</span></span><br/>                  | <span data-ttu-id="c689e-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c689e-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c689e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c689e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c689e-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c689e-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c689e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c689e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c689e-130">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="c689e-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

