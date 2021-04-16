---
title: Mensagem de LB_SETITEMHEIGHT (WinUser. h)
description: Define a altura, em pixels, de itens em uma caixa de listagem. Se a caixa de listagem tiver o \_ estilo de lbs OwnerDrawVariable, essa mensagem definirá a altura do item especificado pelo parâmetro wParam. Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Controles de LB_SETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455754"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="2e616-106">SETITEMHEIGHT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="2e616-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="2e616-107">Define a altura, em pixels, de itens em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2e616-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="2e616-108">Se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) , essa mensagem definirá a altura do item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="2e616-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="2e616-109">Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2e616-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e616-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e616-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e616-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e616-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e616-112">Especifica o índice de base zero do item na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2e616-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="2e616-113">Use esse parâmetro somente se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ; caso contrário, defina-o como zero.</span><span class="sxs-lookup"><span data-stu-id="2e616-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="2e616-114">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e616-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="2e616-115">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="2e616-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="2e616-116">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="2e616-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="2e616-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e616-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e616-118">Especifica a altura, em pixels, do item.</span><span class="sxs-lookup"><span data-stu-id="2e616-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="2e616-119">A altura máxima é de 255 pixels.</span><span class="sxs-lookup"><span data-stu-id="2e616-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e616-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e616-120">Return value</span></span>

<span data-ttu-id="2e616-121">Se o índice ou a altura for inválido, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="2e616-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e616-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e616-122">Requirements</span></span>



| <span data-ttu-id="2e616-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e616-123">Requirement</span></span> | <span data-ttu-id="2e616-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2e616-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e616-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e616-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e616-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e616-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e616-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e616-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e616-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e616-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e616-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e616-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e616-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e616-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e616-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e616-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e616-132">**\_GETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="2e616-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





