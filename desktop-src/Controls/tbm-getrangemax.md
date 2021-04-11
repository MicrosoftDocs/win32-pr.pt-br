---
title: Mensagem de TBM_GETRANGEMAX (commctrl. h)
description: Recupera a posição máxima do controle deslizante em um TrackBar.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- Controles de TBM_GETRANGEMAX de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009396"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="b1a48-104">\_Mensagem tbm GETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="b1a48-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="b1a48-105">Recupera a posição máxima do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b1a48-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1a48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1a48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1a48-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b1a48-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b1a48-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b1a48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1a48-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b1a48-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b1a48-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a48-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1a48-111">Return value</span></span>

<span data-ttu-id="b1a48-112">Retorna um valor de 32 bits que especifica a posição máxima no intervalo de TrackBar de mínimo para máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="b1a48-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a48-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a48-113">Requirements</span></span>



| <span data-ttu-id="b1a48-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a48-114">Requirement</span></span> | <span data-ttu-id="b1a48-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a48-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a48-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a48-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a48-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1a48-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1a48-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a48-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a48-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1a48-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1a48-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1a48-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a48-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a48-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a48-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1a48-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1a48-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b1a48-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1a48-124">**TBM \_ GETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="b1a48-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="b1a48-125">**\_SETRANGE tbm**</span><span class="sxs-lookup"><span data-stu-id="b1a48-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="b1a48-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="b1a48-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





