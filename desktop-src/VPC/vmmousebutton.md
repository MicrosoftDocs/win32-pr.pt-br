---
title: Enumeração VMMouseButton (VPCCOMInterfaces. h)
description: Especifica o botão do mouse.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- VMMouseButton de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455677"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="20fe9-104">Enumeração VMMouseButton</span><span class="sxs-lookup"><span data-stu-id="20fe9-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="20fe9-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20fe9-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="20fe9-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="20fe9-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="20fe9-107">Especifica o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="20fe9-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fe9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="20fe9-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="20fe9-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="20fe9-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="20fe9-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton \_ à esquerda**</span><span class="sxs-lookup"><span data-stu-id="20fe9-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="20fe9-111">O botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="20fe9-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="20fe9-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ à direita**</span><span class="sxs-lookup"><span data-stu-id="20fe9-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="20fe9-113">O botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="20fe9-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="20fe9-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton \_ Center**</span><span class="sxs-lookup"><span data-stu-id="20fe9-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="20fe9-115">O botão central do mouse.</span><span class="sxs-lookup"><span data-stu-id="20fe9-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20fe9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fe9-116">Requirements</span></span>



| <span data-ttu-id="20fe9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fe9-117">Requirement</span></span> | <span data-ttu-id="20fe9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="20fe9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fe9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="20fe9-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="20fe9-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20fe9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fe9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="20fe9-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20fe9-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="20fe9-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="20fe9-123">End of client support</span></span><br/>    | <span data-ttu-id="20fe9-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20fe9-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="20fe9-125">Produto</span><span class="sxs-lookup"><span data-stu-id="20fe9-125">Product</span></span><br/>                  | <span data-ttu-id="20fe9-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="20fe9-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="20fe9-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20fe9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="20fe9-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="20fe9-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fe9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="20fe9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fe9-130">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="20fe9-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

