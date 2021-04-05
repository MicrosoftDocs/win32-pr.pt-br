---
title: Mensagem de WM_DWMCOLORIZATIONCOLORCHANGED (WinUser. h)
description: Informa todas as janelas de nível superior que a cor de colorização alterou.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Mensagem de WM_DWMCOLORIZATIONCOLORCHANGED Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085643"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="d3f78-104">Mensagem do WM \_ DWMCOLORIZATIONCOLORCHANGED</span><span class="sxs-lookup"><span data-stu-id="d3f78-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="d3f78-105">Informa todas as janelas de nível superior que a cor de colorização alterou.</span><span class="sxs-lookup"><span data-stu-id="d3f78-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3f78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3f78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3f78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f78-108">Especifica a nova cor de colorização.</span><span class="sxs-lookup"><span data-stu-id="d3f78-108">Specifies the new colorization color.</span></span> <span data-ttu-id="d3f78-109">O formato de cor é 0xAARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="d3f78-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="d3f78-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3f78-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f78-111">Especifica se a nova cor é mesclada com opacidade.</span><span class="sxs-lookup"><span data-stu-id="d3f78-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f78-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3f78-112">Return value</span></span>

<span data-ttu-id="d3f78-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="d3f78-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f78-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3f78-114">Remarks</span></span>

<span data-ttu-id="d3f78-115">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d3f78-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="d3f78-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) é usado para determinar o valor de cor atual.</span><span class="sxs-lookup"><span data-stu-id="d3f78-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f78-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f78-117">Requirements</span></span>



| <span data-ttu-id="d3f78-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f78-118">Requirement</span></span> | <span data-ttu-id="d3f78-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d3f78-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f78-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3f78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f78-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3f78-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d3f78-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3f78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f78-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3f78-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3f78-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3f78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f78-125"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f78-125"><dt>Winuser.h</dt></span></span> </dl> |



 

