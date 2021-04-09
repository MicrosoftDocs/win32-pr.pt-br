---
title: Mensagem de HDM_ORDERTOINDEX (commctrl. h)
description: Recupera um valor de índice para um item com base em sua ordem no controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro OrderToIndex do cabeçalho.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Controles de HDM_ORDERTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009304"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="bc2ed-105">\_Mensagem HDM ORDERTOINDEX</span><span class="sxs-lookup"><span data-stu-id="bc2ed-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="bc2ed-106">Recupera um valor de índice para um item com base em sua ordem no controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="bc2ed-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ OrderToIndex do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .</span><span class="sxs-lookup"><span data-stu-id="bc2ed-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc2ed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc2ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc2ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2ed-110">A ordem na qual o item aparece dentro do controle de cabeçalho, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="bc2ed-111">Por exemplo, o valor de índice do item na coluna da extrema esquerda seria 0.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="bc2ed-112">O valor do próximo item à direita seria 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="bc2ed-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc2ed-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bc2ed-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2ed-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc2ed-115">Return value</span></span>

<span data-ttu-id="bc2ed-116">Retorna INT que indica o índice do item.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="bc2ed-117">Se *wParam* for inválido (negativo ou muito grande), o retorno será igual a *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bc2ed-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2ed-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc2ed-118">Requirements</span></span>



| <span data-ttu-id="bc2ed-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc2ed-119">Requirement</span></span> | <span data-ttu-id="bc2ed-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bc2ed-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2ed-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc2ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2ed-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc2ed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc2ed-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc2ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2ed-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bc2ed-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc2ed-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc2ed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc2ed-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc2ed-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





