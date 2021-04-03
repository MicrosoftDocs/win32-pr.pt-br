---
title: Mensagem de TTM_SETTITLE (commctrl. h)
description: Adiciona um ícone padrão e uma cadeia de título a uma dica de ferramenta.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- Controles de TTM_SETTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824751"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="e3308-104">Mensagem do TTM \_ SETtitle</span><span class="sxs-lookup"><span data-stu-id="e3308-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="e3308-105">Adiciona um ícone padrão e uma cadeia de título a uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="e3308-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3308-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3308-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3308-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3308-108">Defina *wParam* como um dos valores a seguir para especificar o ícone a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="e3308-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="e3308-109">A partir do Windows XP SP2 e posterior, esse parâmetro também pode conter um valor de **HICON** .</span><span class="sxs-lookup"><span data-stu-id="e3308-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="e3308-110">Um valor maior que TTI \_ é considerado um **HICON**.</span><span class="sxs-lookup"><span data-stu-id="e3308-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="e3308-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e3308-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="e3308-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e3308-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="e3308-113"><dt>**TTI \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="e3308-114">Nenhum ícone.</span><span class="sxs-lookup"><span data-stu-id="e3308-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="e3308-115"><dt>**informações de TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="e3308-116">Ícone de informações.</span><span class="sxs-lookup"><span data-stu-id="e3308-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="e3308-117"><dt>**aviso de TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="e3308-118">Ícone de aviso:</span><span class="sxs-lookup"><span data-stu-id="e3308-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="e3308-119"><dt>**erro de TTI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="e3308-120">Ícone de erro</span><span class="sxs-lookup"><span data-stu-id="e3308-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="e3308-121"><dt>**TTI de \_ informações \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="e3308-122">Ícone de erro grande</span><span class="sxs-lookup"><span data-stu-id="e3308-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="e3308-123"><dt>**TTI de \_ aviso \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="e3308-124">Ícone de erro grande</span><span class="sxs-lookup"><span data-stu-id="e3308-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="e3308-125"><dt>**erro de TTI \_ \_ grande**</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="e3308-126">Ícone de erro grande</span><span class="sxs-lookup"><span data-stu-id="e3308-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e3308-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3308-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3308-128">Ponteiro para a cadeia de caracteres de título.</span><span class="sxs-lookup"><span data-stu-id="e3308-128">Pointer to the title string.</span></span> <span data-ttu-id="e3308-129">Você deve atribuir um valor a *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e3308-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3308-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3308-130">Return value</span></span>

<span data-ttu-id="e3308-131">Retornará **true** se for bem-sucedido, **false** se não.</span><span class="sxs-lookup"><span data-stu-id="e3308-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3308-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3308-132">Remarks</span></span>

<span data-ttu-id="e3308-133">O título de uma dica de ferramenta aparece acima do texto, em uma fonte diferente.</span><span class="sxs-lookup"><span data-stu-id="e3308-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="e3308-134">Não é suficiente ter um título; a dica de ferramenta também deve ter texto ou não é exibida.</span><span class="sxs-lookup"><span data-stu-id="e3308-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="e3308-135">Quando *wParam* contém um **HICON**, uma cópia do ícone é criada pela janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="e3308-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="e3308-136">Ao chamar **TTM \_ SetTitle**, a cadeia de caracteres apontada por *lParam* não deve exceder 100 **TCHARs** de comprimento, incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="e3308-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="e3308-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3308-137">Examples</span></span>

<span data-ttu-id="e3308-138">O exemplo a seguir mostra como adicionar um título e um ícone do sistema a uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="e3308-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="e3308-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3308-139">Requirements</span></span>



| <span data-ttu-id="e3308-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3308-140">Requirement</span></span> | <span data-ttu-id="e3308-141">Valor</span><span class="sxs-lookup"><span data-stu-id="e3308-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3308-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3308-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e3308-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3308-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3308-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3308-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e3308-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3308-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3308-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3308-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3308-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3308-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e3308-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e3308-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e3308-149">**TTM \_ SETTITLEW** (Unicode) e **TTM \_ settítuloa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e3308-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e3308-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3308-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3308-151">Sobre os controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="e3308-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





