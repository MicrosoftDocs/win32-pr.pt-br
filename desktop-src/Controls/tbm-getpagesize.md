---
title: Mensagem de TBM_GETPAGESIZE (commctrl. h)
description: Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Controles de TBM_GETPAGESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085581"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="d854a-104">TBM obter \_ mensagem</span><span class="sxs-lookup"><span data-stu-id="d854a-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="d854a-105">Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d854a-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="d854a-106">As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="d854a-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="d854a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d854a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d854a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d854a-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d854a-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d854a-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d854a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d854a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d854a-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d854a-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d854a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d854a-112">Return value</span></span>

<span data-ttu-id="d854a-113">Retorna um valor de 32 bits que especifica o tamanho da página para o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d854a-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="d854a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d854a-114">Remarks</span></span>

<span data-ttu-id="d854a-115">O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação de TB \_ PageUp e TB \_ PageDown para sua janela pai quando recebe entrada de teclado ou mouse que rola a página.</span><span class="sxs-lookup"><span data-stu-id="d854a-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="d854a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d854a-116">Requirements</span></span>



| <span data-ttu-id="d854a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d854a-117">Requirement</span></span> | <span data-ttu-id="d854a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d854a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d854a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d854a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d854a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d854a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d854a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d854a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d854a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d854a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d854a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d854a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d854a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d854a-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d854a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d854a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d854a-126">**TBM de \_ páginas**</span><span class="sxs-lookup"><span data-stu-id="d854a-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





