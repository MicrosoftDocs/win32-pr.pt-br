---
title: Mensagem de LB_SETTOPINDEX (WinUser. h)
description: Garante que o item especificado em uma caixa de listagem esteja visível.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- Controles de LB_SETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086170"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="4215f-104">SETTOPINDEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="4215f-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="4215f-105">Garante que o item especificado em uma caixa de listagem esteja visível.</span><span class="sxs-lookup"><span data-stu-id="4215f-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="4215f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4215f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4215f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4215f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4215f-108">O índice de base zero do item na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="4215f-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="4215f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4215f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="4215f-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="4215f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="4215f-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="4215f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="4215f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4215f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4215f-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="4215f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4215f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4215f-114">Return value</span></span>

<span data-ttu-id="4215f-115">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="4215f-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="4215f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4215f-116">Remarks</span></span>

<span data-ttu-id="4215f-117">O sistema rola o conteúdo da caixa de listagem para que o item especificado seja exibido na parte superior da caixa de listagem ou o intervalo máximo de rolagem tenha sido atingido.</span><span class="sxs-lookup"><span data-stu-id="4215f-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="4215f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4215f-118">Requirements</span></span>



| <span data-ttu-id="4215f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4215f-119">Requirement</span></span> | <span data-ttu-id="4215f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4215f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4215f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4215f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4215f-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4215f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4215f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4215f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4215f-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4215f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4215f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4215f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4215f-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4215f-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4215f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4215f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4215f-128">**\_GETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="4215f-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





