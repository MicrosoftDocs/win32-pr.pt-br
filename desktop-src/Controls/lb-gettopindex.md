---
title: Mensagem de LB_GETTOPINDEX (WinUser. h)
description: Obtém o índice do primeiro item visível em uma caixa de listagem.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Controles de LB_GETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918486"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="5e955-104">GETTOPINDEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="5e955-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="5e955-105">Obtém o índice do primeiro item visível em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="5e955-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="5e955-106">Inicialmente, o item com o índice 0 está na parte superior da caixa de listagem, mas se o conteúdo da caixa de listagem tiver sido rolado, outro item poderá estar na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5e955-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="5e955-107">O primeiro item visível em uma caixa de listagem de várias colunas é o item superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="5e955-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e955-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e955-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e955-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e955-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e955-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e955-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e955-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e955-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e955-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e955-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e955-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e955-113">Return value</span></span>

<span data-ttu-id="5e955-114">O valor de retorno é o índice do primeiro item visível na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="5e955-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e955-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e955-115">Requirements</span></span>



| <span data-ttu-id="5e955-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e955-116">Requirement</span></span> | <span data-ttu-id="5e955-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5e955-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e955-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e955-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e955-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e955-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e955-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e955-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e955-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e955-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e955-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e955-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e955-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e955-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e955-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e955-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e955-125">**\_SETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="5e955-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





