---
title: Mensagem de TBM_SETLINESIZE (commctrl. h)
description: Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- Controles de TBM_SETLINESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918116"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="0f776-105">TBM \_ SETlinhasize mensagem</span><span class="sxs-lookup"><span data-stu-id="0f776-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="0f776-106">Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou.</span><span class="sxs-lookup"><span data-stu-id="0f776-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="0f776-107">As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0f776-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f776-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f776-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f776-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f776-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f776-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0f776-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f776-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f776-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f776-112">Novo tamanho da linha.</span><span class="sxs-lookup"><span data-stu-id="0f776-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f776-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f776-113">Return value</span></span>

<span data-ttu-id="0f776-114">Retorna um valor de 32 bits que especifica o tamanho da linha anterior.</span><span class="sxs-lookup"><span data-stu-id="0f776-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f776-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f776-115">Remarks</span></span>

<span data-ttu-id="0f776-116">A configuração padrão para o tamanho da linha é 1.</span><span class="sxs-lookup"><span data-stu-id="0f776-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="0f776-117">O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação da lista de TB \_ e TB \_ LINEDOWN para sua janela pai quando o usuário pressiona as teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="0f776-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f776-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f776-118">Requirements</span></span>



| <span data-ttu-id="0f776-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f776-119">Requirement</span></span> | <span data-ttu-id="0f776-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0f776-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f776-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f776-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f776-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f776-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f776-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f776-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f776-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f776-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f776-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f776-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f776-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f776-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f776-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f776-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f776-128">**TBM \_ GETlines**</span><span class="sxs-lookup"><span data-stu-id="0f776-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





