---
title: Mensagem de HDM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro InsertItem do cabeçalho.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Controles de HDM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455180"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="33ceb-105">\_Mensagem HDM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="33ceb-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="33ceb-106">Insere um novo item em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="33ceb-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="33ceb-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ InsertItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="33ceb-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33ceb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33ceb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ceb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33ceb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33ceb-110">O índice do item após o qual o novo item deve ser inserido.</span><span class="sxs-lookup"><span data-stu-id="33ceb-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="33ceb-111">O novo item será inserido no final do controle de cabeçalho se *wParam* for maior ou igual ao número de itens no controle.</span><span class="sxs-lookup"><span data-stu-id="33ceb-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="33ceb-112">Se *wParam* for zero, o novo item será inserido no início do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="33ceb-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="33ceb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33ceb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33ceb-114">Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contém informações sobre o novo item.</span><span class="sxs-lookup"><span data-stu-id="33ceb-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ceb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33ceb-115">Return value</span></span>

<span data-ttu-id="33ceb-116">Retorna o índice do novo item se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="33ceb-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ceb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ceb-117">Requirements</span></span>



| <span data-ttu-id="33ceb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ceb-118">Requirement</span></span> | <span data-ttu-id="33ceb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="33ceb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33ceb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33ceb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33ceb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33ceb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33ceb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33ceb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33ceb-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33ceb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33ceb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33ceb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33ceb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ceb-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="33ceb-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="33ceb-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="33ceb-127">**HDM \_ INSERTITEMW** (Unicode) e **HDM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="33ceb-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





