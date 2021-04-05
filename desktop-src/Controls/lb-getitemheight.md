---
title: Mensagem de LB_GETITEMHEIGHT (WinUser. h)
description: Obtém a altura dos itens em uma caixa de listagem.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Controles de LB_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824338"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="63b5e-104">GETITEMHEIGHT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="63b5e-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="63b5e-105">Obtém a altura dos itens em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="63b5e-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="63b5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63b5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b5e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63b5e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63b5e-108">O índice de base zero do item da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="63b5e-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="63b5e-109">Esse índice será usado somente se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ; caso contrário, ela deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="63b5e-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="63b5e-110">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="63b5e-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="63b5e-111">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="63b5e-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="63b5e-112">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="63b5e-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="63b5e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63b5e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63b5e-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="63b5e-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b5e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63b5e-115">Return value</span></span>

<span data-ttu-id="63b5e-116">O valor de retorno é a altura, em pixels, de cada item na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="63b5e-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="63b5e-117">O valor de retorno é a altura do item especificado pelo parâmetro *wParam* se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="63b5e-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="63b5e-118">O valor de retorno será um erro de LB \_ se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="63b5e-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b5e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63b5e-119">Requirements</span></span>



| <span data-ttu-id="63b5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b5e-120">Requirement</span></span> | <span data-ttu-id="63b5e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="63b5e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b5e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b5e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="63b5e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63b5e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63b5e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b5e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="63b5e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63b5e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63b5e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63b5e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b5e-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63b5e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b5e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="63b5e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b5e-129">**\_SETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="63b5e-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





