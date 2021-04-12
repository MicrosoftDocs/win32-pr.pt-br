---
title: Mensagem de CB_SETEDITSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETEDITSEL CB para selecionar caracteres no controle de edição de uma caixa de combinação.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Controles de CB_SETEDITSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455118"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="dfdeb-104">\_Mensagem de SETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="dfdeb-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="dfdeb-105">Um aplicativo envia uma mensagem de **\_ SETEDITSEL CB** para selecionar caracteres no controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfdeb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfdeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfdeb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfdeb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfdeb-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dfdeb-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfdeb-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdeb-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="dfdeb-111">Se **LOWORD** for-1, a seleção, se houver, será removida.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="dfdeb-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* especifica a posição final.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="dfdeb-113">Se **HIWORD** for-1, todo o texto da posição inicial para o último caractere no controle de edição será selecionado.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfdeb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfdeb-114">Return value</span></span>

<span data-ttu-id="dfdeb-115">Se a mensagem tiver sucesso, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="dfdeb-116">Se a mensagem for enviada para uma caixa de combinação com o estilo do [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfdeb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfdeb-117">Remarks</span></span>

<span data-ttu-id="dfdeb-118">As posições são baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-118">The positions are zero-based.</span></span> <span data-ttu-id="dfdeb-119">O primeiro caractere do controle de edição está na posição zero.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="dfdeb-120">O primeiro caractere após o último caractere selecionado está na posição final.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="dfdeb-121">Por exemplo, para selecionar os quatro primeiros caracteres do controle de edição, use uma posição inicial de 0 e uma posição final de 4.</span><span class="sxs-lookup"><span data-stu-id="dfdeb-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfdeb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfdeb-122">Requirements</span></span>



| <span data-ttu-id="dfdeb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfdeb-123">Requirement</span></span> | <span data-ttu-id="dfdeb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dfdeb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdeb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfdeb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dfdeb-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfdeb-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfdeb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfdeb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dfdeb-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfdeb-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dfdeb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfdeb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfdeb-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfdeb-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfdeb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfdeb-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="dfdeb-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dfdeb-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dfdeb-133">**\_GETEDITSEL CB**</span><span class="sxs-lookup"><span data-stu-id="dfdeb-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="dfdeb-134">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="dfdeb-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dfdeb-135">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="dfdeb-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

