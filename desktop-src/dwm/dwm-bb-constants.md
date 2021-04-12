---
title: Desfoque de DWM por trás de constantes (dwmapi. h)
description: Sinalizadores usados pela estrutura DWM \_ BLURBEHIND para indicar quais dos seus membros contêm informações válidas.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499492"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="17344-103">Desfoque de DWM por trás de constantes</span><span class="sxs-lookup"><span data-stu-id="17344-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="17344-104">Sinalizadores usados pela estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar quais dos seus membros contêm informações válidas.</span><span class="sxs-lookup"><span data-stu-id="17344-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="17344-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ habilitar**</span><span class="sxs-lookup"><span data-stu-id="17344-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17344-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="17344-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="17344-107">Um valor para o membro **fEnable** foi especificado.</span><span class="sxs-lookup"><span data-stu-id="17344-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17344-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**</span><span class="sxs-lookup"><span data-stu-id="17344-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17344-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="17344-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="17344-110">Um valor para o membro **hRgnBlur** foi especificado.</span><span class="sxs-lookup"><span data-stu-id="17344-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17344-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**</span><span class="sxs-lookup"><span data-stu-id="17344-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17344-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="17344-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="17344-113">Um valor para o membro **fTransitionOnMaximized** foi especificado.</span><span class="sxs-lookup"><span data-stu-id="17344-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17344-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17344-114">Requirements</span></span>



| <span data-ttu-id="17344-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="17344-115">Requirement</span></span> | <span data-ttu-id="17344-116">Valor</span><span class="sxs-lookup"><span data-stu-id="17344-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17344-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17344-117">Minimum supported client</span></span><br/> | <span data-ttu-id="17344-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17344-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17344-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17344-119">Minimum supported server</span></span><br/> | <span data-ttu-id="17344-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17344-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="17344-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17344-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="17344-122"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17344-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





