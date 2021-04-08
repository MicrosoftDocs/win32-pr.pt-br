---
title: Mensagem de CB_SETCURSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem do CB setcurse para selecionar uma cadeia de caracteres na lista de uma caixa de combinação.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Controles de CB_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009351"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="45b95-104">Mensagem do CB \_ SETcurseal</span><span class="sxs-lookup"><span data-stu-id="45b95-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="45b95-105">Um aplicativo envia uma mensagem do **CB \_ setcurse** para selecionar uma cadeia de caracteres na lista de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="45b95-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="45b95-106">Se necessário, a lista rola a cadeia de caracteres para a exibição.</span><span class="sxs-lookup"><span data-stu-id="45b95-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="45b95-107">O texto no controle de edição da caixa de combinação é alterado para refletir a nova seleção e qualquer seleção anterior na lista é removida.</span><span class="sxs-lookup"><span data-stu-id="45b95-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="45b95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45b95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b95-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45b95-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45b95-110">Especifica o índice de base zero da cadeia de caracteres a ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="45b95-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="45b95-111">Se esse parâmetro for-1, qualquer seleção atual na lista será removida e o controle de edição será limpo.</span><span class="sxs-lookup"><span data-stu-id="45b95-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="45b95-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45b95-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45b95-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="45b95-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b95-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45b95-114">Return value</span></span>

<span data-ttu-id="45b95-115">Se a mensagem for bem-sucedida, o valor de retorno será o índice do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="45b95-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="45b95-116">Se *wParam* for maior do que o número de itens na lista ou se *wParam* for-1, o valor de retorno será CB \_ Err e a seleção será desmarcada.</span><span class="sxs-lookup"><span data-stu-id="45b95-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b95-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b95-117">Requirements</span></span>



| <span data-ttu-id="45b95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b95-118">Requirement</span></span> | <span data-ttu-id="45b95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="45b95-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b95-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45b95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45b95-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45b95-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45b95-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45b95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45b95-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45b95-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="45b95-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45b95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b95-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45b95-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b95-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="45b95-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="45b95-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="45b95-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="45b95-128">**localização da CB \_**</span><span class="sxs-lookup"><span data-stu-id="45b95-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="45b95-129">**iscursel de CB \_**</span><span class="sxs-lookup"><span data-stu-id="45b95-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="45b95-130">**seleção do CB \_**</span><span class="sxs-lookup"><span data-stu-id="45b95-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





