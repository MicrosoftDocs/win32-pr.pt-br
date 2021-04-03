---
title: Mensagem de RB_INSERTBAND (commctrl. h)
description: Insere uma nova faixa em um controle rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Controles de RB_INSERTBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824850"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="b86b0-104">\_Mensagem INSERTBAND RB</span><span class="sxs-lookup"><span data-stu-id="b86b0-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="b86b0-105">Insere uma nova faixa em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b86b0-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b86b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b86b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b86b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b86b0-108">Índice de base zero do local onde a banda será inserida.</span><span class="sxs-lookup"><span data-stu-id="b86b0-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="b86b0-109">Se você definir esse parâmetro como-1, o controle adicionará a nova banda no último local.</span><span class="sxs-lookup"><span data-stu-id="b86b0-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="b86b0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b86b0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b86b0-111">Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define a banda a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="b86b0-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="b86b0-112">Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(REBARBANDINFO) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="b86b0-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86b0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b86b0-113">Return value</span></span>

<span data-ttu-id="b86b0-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="b86b0-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86b0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b86b0-115">Requirements</span></span>



| <span data-ttu-id="b86b0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b86b0-116">Requirement</span></span> | <span data-ttu-id="b86b0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b86b0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b86b0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b86b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b86b0-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b86b0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b86b0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b86b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b86b0-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b86b0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b86b0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b86b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86b0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86b0-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b86b0-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b86b0-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b86b0-125">**RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b86b0-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





