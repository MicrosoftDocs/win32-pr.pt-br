---
title: Mensagem de CBEM_DELETEITEM (commctrl. h)
description: Remove um item de um controle ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Controles de CBEM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811146"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="55c25-104">\_Mensagem CBEM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="55c25-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="55c25-105">Remove um item de um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="55c25-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="55c25-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55c25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c25-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55c25-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55c25-108">O índice de base zero do item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="55c25-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="55c25-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55c25-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="55c25-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="55c25-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c25-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55c25-111">Return value</span></span>

<span data-ttu-id="55c25-112">Retorna um valor INT que representa o número de itens restantes no controle.</span><span class="sxs-lookup"><span data-stu-id="55c25-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="55c25-113">Se *iIndex* for inválido, a mensagem retornará um \_ erro CB.</span><span class="sxs-lookup"><span data-stu-id="55c25-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c25-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c25-114">Remarks</span></span>

<span data-ttu-id="55c25-115">Essa mensagem é mapeada para a caixa de combinação de controle da mensagem [**CB \_ excluirstring**](cb-deletestring.md).</span><span class="sxs-lookup"><span data-stu-id="55c25-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c25-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55c25-116">Requirements</span></span>



| <span data-ttu-id="55c25-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c25-117">Requirement</span></span> | <span data-ttu-id="55c25-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55c25-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55c25-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c25-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55c25-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55c25-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55c25-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c25-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55c25-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55c25-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55c25-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55c25-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c25-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c25-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





