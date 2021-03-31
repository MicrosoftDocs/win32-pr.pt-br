---
title: Mensagem de LB_GETSEL (WinUser. h)
description: Obtém o estado de seleção de um item.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- Controles de LB_GETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824520"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="87d98-104">GETSEL de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="87d98-104">LB\_GETSEL message</span></span>

<span data-ttu-id="87d98-105">Obtém o estado de seleção de um item.</span><span class="sxs-lookup"><span data-stu-id="87d98-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="87d98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87d98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87d98-108">O índice de base zero do item.</span><span class="sxs-lookup"><span data-stu-id="87d98-108">The zero-based index of the item.</span></span>

<span data-ttu-id="87d98-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="87d98-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="87d98-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="87d98-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="87d98-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="87d98-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="87d98-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87d98-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87d98-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="87d98-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d98-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87d98-114">Return value</span></span>

<span data-ttu-id="87d98-115">Se um item for selecionado, o valor de retorno será maior que zero; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="87d98-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="87d98-116">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="87d98-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d98-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87d98-117">Requirements</span></span>



| <span data-ttu-id="87d98-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d98-118">Requirement</span></span> | <span data-ttu-id="87d98-119">Valor</span><span class="sxs-lookup"><span data-stu-id="87d98-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d98-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87d98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87d98-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87d98-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="87d98-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87d98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87d98-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87d98-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87d98-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87d98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d98-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87d98-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d98-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87d98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d98-127">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="87d98-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





