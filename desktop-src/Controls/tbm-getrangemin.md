---
title: Mensagem de TBM_GETRANGEMIN (commctrl. h)
description: Recupera a posição mínima do controle deslizante em um TrackBar.
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- Controles de TBM_GETRANGEMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918481"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="26cbc-104">\_Mensagem tbm GETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="26cbc-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="26cbc-105">Recupera a posição mínima do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="26cbc-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="26cbc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26cbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26cbc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26cbc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26cbc-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="26cbc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26cbc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26cbc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26cbc-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="26cbc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26cbc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26cbc-111">Return value</span></span>

<span data-ttu-id="26cbc-112">Retorna um valor de 32 bits que especifica a posição mínima no intervalo de TrackBar de mínimo para posições de controle deslizante máximo.</span><span class="sxs-lookup"><span data-stu-id="26cbc-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="26cbc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26cbc-113">Requirements</span></span>



| <span data-ttu-id="26cbc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="26cbc-114">Requirement</span></span> | <span data-ttu-id="26cbc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="26cbc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26cbc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26cbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="26cbc-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26cbc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26cbc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26cbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="26cbc-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26cbc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26cbc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26cbc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="26cbc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26cbc-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26cbc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="26cbc-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="26cbc-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="26cbc-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26cbc-124">**TBM \_ GETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="26cbc-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="26cbc-125">**\_SETRANGE tbm**</span><span class="sxs-lookup"><span data-stu-id="26cbc-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="26cbc-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="26cbc-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





