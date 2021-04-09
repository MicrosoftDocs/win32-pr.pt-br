---
title: Mensagem de TBM_SETPAGESIZE (commctrl. h)
description: Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Controles de TBM_SETPAGESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009598"
---
# <a name="tbm_setpagesize-message"></a><span data-ttu-id="dd731-104">TBMr a \_ mensagem de página</span><span class="sxs-lookup"><span data-stu-id="dd731-104">TBM\_SETPAGESIZE message</span></span>

<span data-ttu-id="dd731-105">Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dd731-105">Sets the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="dd731-106">As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="dd731-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd731-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd731-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd731-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd731-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd731-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dd731-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dd731-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd731-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd731-111">Novo tamanho da página.</span><span class="sxs-lookup"><span data-stu-id="dd731-111">New page size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd731-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd731-112">Return value</span></span>

<span data-ttu-id="dd731-113">Retorna um valor de 32 bits que especifica o tamanho da página anterior.</span><span class="sxs-lookup"><span data-stu-id="dd731-113">Returns a 32-bit value that specifies the previous page size.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd731-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd731-114">Remarks</span></span>

<span data-ttu-id="dd731-115">O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação de TB \_ PageUp e TB \_ PageDown para sua janela pai quando recebe entrada de teclado ou mouse que rola a página.</span><span class="sxs-lookup"><span data-stu-id="dd731-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd731-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd731-116">Requirements</span></span>



| <span data-ttu-id="dd731-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd731-117">Requirement</span></span> | <span data-ttu-id="dd731-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dd731-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd731-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd731-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd731-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd731-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd731-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd731-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd731-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd731-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd731-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd731-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd731-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd731-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd731-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd731-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd731-126">**TBM \_ GETpagesize**</span><span class="sxs-lookup"><span data-stu-id="dd731-126">**TBM\_GETPAGESIZE**</span></span>](tbm-getpagesize.md)
</dt> </dl>

 

 





