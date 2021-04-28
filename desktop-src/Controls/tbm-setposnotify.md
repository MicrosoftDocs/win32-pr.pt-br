---
title: Mensagem de TBM_SETPOSNOTIFY (commctrl. h)
description: TBM_SETPOSNOTIFY mensagem – define a posição lógica atual do controle deslizante em um TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Controles de TBM_SETPOSNOTIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104074"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="f8ddf-104">\_Mensagem tbm SETPOSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="f8ddf-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="f8ddf-105">Define a posição lógica atual do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8ddf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8ddf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ddf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8ddf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ddf-108">wParam não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="f8ddf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8ddf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ddf-110">Nova posição lógica do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-110">New logical position of the slider.</span></span> <span data-ttu-id="f8ddf-111">As posições lógicas válidas são os valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="f8ddf-112">Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ddf-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8ddf-113">Return value</span></span>

<span data-ttu-id="f8ddf-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f8ddf-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ddf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8ddf-115">Remarks</span></span>

<span data-ttu-id="f8ddf-116">Chamar **tbm \_ SETPOSNOTIFY** definirá o local do controle deslizante TrackBar como [**tbm \_ SETPOS**](tbm-setpos.md) , mas também fará com que o TrackBar Notifique seu pai de uma movimentação por meio de uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ddf-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ddf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8ddf-117">Requirements</span></span>



| <span data-ttu-id="f8ddf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ddf-118">Requirement</span></span> | <span data-ttu-id="f8ddf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ddf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ddf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8ddf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ddf-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f8ddf-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f8ddf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8ddf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ddf-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f8ddf-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8ddf-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8ddf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ddf-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





