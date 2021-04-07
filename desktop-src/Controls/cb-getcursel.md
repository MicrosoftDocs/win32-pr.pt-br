---
title: Mensagem de CB_GETCURSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de IScursel de CB para recuperar o índice do item atualmente selecionado, se houver, na caixa de listagem de uma caixa de combinação.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Controles de CB_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824871"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="ade52-104">\_Mensagem de ISCURSE CB</span><span class="sxs-lookup"><span data-stu-id="ade52-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="ade52-105">Um aplicativo envia uma mensagem de **\_ iscursel de CB** para recuperar o índice do item atualmente selecionado, se houver, na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="ade52-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ade52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ade52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade52-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ade52-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ade52-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ade52-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ade52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ade52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ade52-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ade52-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade52-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ade52-111">Return value</span></span>

<span data-ttu-id="ade52-112">O valor de retorno é o índice de base zero do item selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ade52-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="ade52-113">Se nenhum item for selecionado, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ade52-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade52-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade52-114">Requirements</span></span>



| <span data-ttu-id="ade52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade52-115">Requirement</span></span> | <span data-ttu-id="ade52-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ade52-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade52-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ade52-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ade52-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ade52-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ade52-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ade52-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ade52-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ade52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade52-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ade52-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade52-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ade52-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ade52-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ade52-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ade52-125">**seleção do CB \_**</span><span class="sxs-lookup"><span data-stu-id="ade52-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="ade52-126">**CB \_ SETcurseal**</span><span class="sxs-lookup"><span data-stu-id="ade52-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





