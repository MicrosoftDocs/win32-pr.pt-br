---
title: Enumeração VMStartupOption (VPCCOMInterfaces. h)
description: Especifica a opção de inicialização.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- VMStartupOption de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455087"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="b6d9e-104">Enumeração VMStartupOption</span><span class="sxs-lookup"><span data-stu-id="b6d9e-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="b6d9e-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6d9e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b6d9e-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6d9e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b6d9e-107">Especifica a opção de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b6d9e-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d9e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6d9e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="b6d9e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="b6d9e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b6d9e-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ normal**</span><span class="sxs-lookup"><span data-stu-id="b6d9e-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="b6d9e-111">Inicie normalmente.</span><span class="sxs-lookup"><span data-stu-id="b6d9e-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="b6d9e-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption \_ FixParentTimestampMismatch**</span><span class="sxs-lookup"><span data-stu-id="b6d9e-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="b6d9e-113">Corrija a incompatibilidade de carimbo de data/hora pai.</span><span class="sxs-lookup"><span data-stu-id="b6d9e-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6d9e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d9e-114">Requirements</span></span>



| <span data-ttu-id="b6d9e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d9e-115">Requirement</span></span> | <span data-ttu-id="b6d9e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b6d9e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d9e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6d9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d9e-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6d9e-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6d9e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6d9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d9e-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b6d9e-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b6d9e-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b6d9e-121">End of client support</span></span><br/>    | <span data-ttu-id="b6d9e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6d9e-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b6d9e-123">Produto</span><span class="sxs-lookup"><span data-stu-id="b6d9e-123">Product</span></span><br/>                  | <span data-ttu-id="b6d9e-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b6d9e-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b6d9e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6d9e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d9e-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d9e-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6d9e-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b6d9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d9e-128">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="b6d9e-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

