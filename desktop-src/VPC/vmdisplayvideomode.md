---
title: Enumeração VMDisplayVideoMode (VPCCOMInterfaces. h)
description: Especifica o modo de vídeo de exibição.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- VMDisplayVideoMode de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455089"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="cb62e-104">Enumeração VMDisplayVideoMode</span><span class="sxs-lookup"><span data-stu-id="cb62e-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="cb62e-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb62e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb62e-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb62e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb62e-107">Especifica o modo de vídeo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cb62e-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb62e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb62e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="cb62e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="cb62e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cb62e-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode \_ TextMode**</span><span class="sxs-lookup"><span data-stu-id="cb62e-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="cb62e-111">Modo de texto.</span><span class="sxs-lookup"><span data-stu-id="cb62e-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="cb62e-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode \_ CGAMode**</span><span class="sxs-lookup"><span data-stu-id="cb62e-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="cb62e-113">Modo CGA.</span><span class="sxs-lookup"><span data-stu-id="cb62e-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="cb62e-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode \_ VGAMode**</span><span class="sxs-lookup"><span data-stu-id="cb62e-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="cb62e-115">Modo VGA.</span><span class="sxs-lookup"><span data-stu-id="cb62e-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="cb62e-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode \_ svgamode**</span><span class="sxs-lookup"><span data-stu-id="cb62e-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="cb62e-117">Modo SVGA.</span><span class="sxs-lookup"><span data-stu-id="cb62e-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb62e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb62e-118">Requirements</span></span>



| <span data-ttu-id="cb62e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb62e-119">Requirement</span></span> | <span data-ttu-id="cb62e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cb62e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb62e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb62e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cb62e-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb62e-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb62e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb62e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cb62e-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cb62e-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb62e-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cb62e-125">End of client support</span></span><br/>    | <span data-ttu-id="cb62e-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb62e-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb62e-127">Produto</span><span class="sxs-lookup"><span data-stu-id="cb62e-127">Product</span></span><br/>                  | <span data-ttu-id="cb62e-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb62e-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb62e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb62e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb62e-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb62e-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb62e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb62e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb62e-132">**IVMDisplay:: videomode**</span><span class="sxs-lookup"><span data-stu-id="cb62e-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

