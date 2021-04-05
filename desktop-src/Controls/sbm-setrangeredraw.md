---
title: Mensagem de SBM_SETRANGEREDRAW (WinUser. h)
description: Um aplicativo envia a \_ mensagem SBM SETRANGEREDRAW para um controle de barra de rolagem para definir os valores de posição mínimo e máximo e redesenhar o controle.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Controles de SBM_SETRANGEREDRAW de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008850"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="0926b-104">\_Mensagem SBM SETRANGEREDRAW</span><span class="sxs-lookup"><span data-stu-id="0926b-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="0926b-105">Um aplicativo envia a mensagem **SBM \_ SETRANGEREDRAW** para um controle de barra de rolagem para definir os valores de posição mínimo e máximo e redesenhar o controle.</span><span class="sxs-lookup"><span data-stu-id="0926b-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0926b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0926b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0926b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0926b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0926b-108">Especifica a posição de rolagem mínima.</span><span class="sxs-lookup"><span data-stu-id="0926b-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="0926b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0926b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0926b-110">Especifica a posição máxima da rolagem.</span><span class="sxs-lookup"><span data-stu-id="0926b-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0926b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0926b-111">Return value</span></span>

<span data-ttu-id="0926b-112">**ComCtl32.dll versão 5,0**: se a posição da caixa de rolagem foi alterada, o valor de retorno será a posição anterior da caixa de rolagem; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="0926b-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="0926b-113">**ComCtl32.dll versão 6,0**: a posição atual da caixa de rolagem, independentemente se ela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="0926b-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0926b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0926b-114">Remarks</span></span>

<span data-ttu-id="0926b-115">Os valores de posição mínimo e máximo padrão são zero.</span><span class="sxs-lookup"><span data-stu-id="0926b-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="0926b-116">A diferença entre os valores especificados pelos parâmetros *wParam* e *lParam* não deve ser maior que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="0926b-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="0926b-117">Se os valores mínimo e máximo da posição forem iguais, o controle da barra de rolagem ficará oculto e, em vigor, desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0926b-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0926b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0926b-118">Requirements</span></span>



| <span data-ttu-id="0926b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0926b-119">Requirement</span></span> | <span data-ttu-id="0926b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0926b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0926b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0926b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0926b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0926b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0926b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0926b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0926b-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0926b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0926b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0926b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0926b-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0926b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0926b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0926b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0926b-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0926b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0926b-129">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="0926b-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="0926b-130">**GetRange SBM \_**</span><span class="sxs-lookup"><span data-stu-id="0926b-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="0926b-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="0926b-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="0926b-132">**\_SETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="0926b-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





