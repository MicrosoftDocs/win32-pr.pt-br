---
title: Mensagem de CB_GETITEMHEIGHT (WinUser. h)
description: Determina a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Controles de CB_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824408"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="d7f0c-104">\_Mensagem de GETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="d7f0c-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="d7f0c-105">Determina a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7f0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f0c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7f0c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f0c-108">O componente da caixa de combinação cuja altura deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="d7f0c-109">Esse parâmetro deve ser-1 para recuperar a altura do campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="d7f0c-110">Ele deve ser zero para recuperar a altura dos itens de lista, a menos que a caixa de combinação tenha o estilo [**\_ OwnerDrawVariable do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d7f0c-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="d7f0c-111">Nesse caso, o parâmetro *wParam* é o índice de base zero de um item de lista específico.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7f0c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f0c-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f0c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7f0c-114">Return value</span></span>

<span data-ttu-id="d7f0c-115">O valor de retorno é a altura, em pixels, dos itens da lista em uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="d7f0c-116">Se a caixa de combinação tiver o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , será a altura do item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d7f0c-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="d7f0c-117">Se *wParam* for-1, o valor de retorno será a altura da parte do controle de edição (ou texto estático) da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="d7f0c-118">Se ocorrer um erro, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d7f0c-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f0c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f0c-119">Requirements</span></span>



| <span data-ttu-id="d7f0c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f0c-120">Requirement</span></span> | <span data-ttu-id="d7f0c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f0c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f0c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f0c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7f0c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d7f0c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f0c-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7f0c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d7f0c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7f0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f0c-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f0c-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d7f0c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7f0c-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d7f0c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7f0c-130">**\_SETITEMHEIGHT CB**</span><span class="sxs-lookup"><span data-stu-id="d7f0c-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="d7f0c-131">**MEASUREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d7f0c-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





