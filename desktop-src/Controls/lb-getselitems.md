---
title: Mensagem de LB_GETSELITEMS (WinUser. h)
description: Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Controles de LB_GETSELITEMS de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918523"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="d8899-104">GETSELITEMS de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="d8899-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="d8899-105">Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="d8899-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8899-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8899-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8899-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8899-108">O número máximo de itens selecionados cujos números de item devem ser colocados no buffer.</span><span class="sxs-lookup"><span data-stu-id="d8899-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="d8899-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d8899-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="d8899-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="d8899-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="d8899-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="d8899-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="d8899-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8899-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8899-113">Um ponteiro para um buffer grande o suficiente para o número de inteiros especificados pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d8899-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8899-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8899-114">Return value</span></span>

<span data-ttu-id="d8899-115">O valor de retorno é o número de itens colocados no buffer.</span><span class="sxs-lookup"><span data-stu-id="d8899-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="d8899-116">Se a caixa de listagem for uma caixa de listagem de seleção única, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="d8899-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8899-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8899-117">Requirements</span></span>



| <span data-ttu-id="d8899-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8899-118">Requirement</span></span> | <span data-ttu-id="d8899-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d8899-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8899-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8899-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8899-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8899-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8899-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8899-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8899-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8899-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d8899-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8899-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8899-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8899-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8899-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8899-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8899-127">**\_GETSELCOUNT lb**</span><span class="sxs-lookup"><span data-stu-id="d8899-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 





