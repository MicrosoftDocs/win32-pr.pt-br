---
title: Mensagem de LB_SETANCHORINDEX (WinUser. h)
description: Define o item de âncora \ 8212; ou seja, o item do qual uma seleção múltipla é iniciada. Uma seleção múltipla abrange todos os itens do item de âncora para o item de cursor.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Controles de LB_SETANCHORINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086175"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="140a6-105">SETANCHORINDEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="140a6-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="140a6-106">Define o item de âncora que é o item do qual uma seleção múltipla é iniciada.</span><span class="sxs-lookup"><span data-stu-id="140a6-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="140a6-107">Uma seleção múltipla abrange todos os itens do item de âncora para o item de cursor.</span><span class="sxs-lookup"><span data-stu-id="140a6-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="140a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="140a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="140a6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="140a6-110">Especifica o índice do novo item de âncora.</span><span class="sxs-lookup"><span data-stu-id="140a6-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="140a6-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="140a6-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="140a6-112">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="140a6-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="140a6-113">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="140a6-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="140a6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="140a6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="140a6-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="140a6-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140a6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="140a6-116">Return value</span></span>

<span data-ttu-id="140a6-117">Se a mensagem tiver sucesso, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="140a6-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="140a6-118">Se a mensagem falhar, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="140a6-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="140a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140a6-119">Requirements</span></span>



| <span data-ttu-id="140a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="140a6-120">Requirement</span></span> | <span data-ttu-id="140a6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="140a6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140a6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="140a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="140a6-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="140a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="140a6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="140a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="140a6-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="140a6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="140a6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="140a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="140a6-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="140a6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140a6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="140a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140a6-129">**\_GETANCHORINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="140a6-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





