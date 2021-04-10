---
title: Mensagem de TBM_GETLINESIZE (commctrl. h)
description: Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Controles de TBM_GETLINESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919225"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="c268b-105">TBM \_ GETlinhasize mensagem</span><span class="sxs-lookup"><span data-stu-id="c268b-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="c268b-106">Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou.</span><span class="sxs-lookup"><span data-stu-id="c268b-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="c268b-107">As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="c268b-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="c268b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c268b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c268b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c268b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c268b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c268b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c268b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c268b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c268b-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c268b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c268b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c268b-113">Return value</span></span>

<span data-ttu-id="c268b-114">Retorna um valor de 32 bits que especifica o tamanho da linha para o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c268b-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="c268b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c268b-115">Remarks</span></span>

<span data-ttu-id="c268b-116">A configuração padrão para o tamanho da linha é 1.</span><span class="sxs-lookup"><span data-stu-id="c268b-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="c268b-117">O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação da lista de TB \_ e TB \_ LINEDOWN para sua janela pai quando o usuário pressiona as teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="c268b-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="c268b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c268b-118">Requirements</span></span>



| <span data-ttu-id="c268b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c268b-119">Requirement</span></span> | <span data-ttu-id="c268b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c268b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c268b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c268b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c268b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c268b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c268b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c268b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c268b-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c268b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c268b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c268b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c268b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c268b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





