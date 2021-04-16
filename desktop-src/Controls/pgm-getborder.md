---
title: Mensagem de PGM_GETBORDER (commctrl. h)
description: Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBorder do pager.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Controles de PGM_GETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753791"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="9cbc6-105">\_Mensagem GETborder do PGM</span><span class="sxs-lookup"><span data-stu-id="9cbc6-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="9cbc6-106">Recupera o tamanho da borda atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="9cbc6-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="9cbc6-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .</span><span class="sxs-lookup"><span data-stu-id="9cbc6-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cbc6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cbc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbc6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cbc6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9cbc6-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9cbc6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9cbc6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cbc6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9cbc6-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9cbc6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cbc6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cbc6-113">Return value</span></span>

<span data-ttu-id="9cbc6-114">Retorna um valor INT que contém o tamanho da borda atual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="9cbc6-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cbc6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbc6-115">Requirements</span></span>



| <span data-ttu-id="9cbc6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbc6-116">Requirement</span></span> | <span data-ttu-id="9cbc6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbc6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbc6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbc6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9cbc6-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cbc6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cbc6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbc6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9cbc6-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cbc6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cbc6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cbc6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cbc6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cbc6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbc6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbc6-125">**SetBorder do PGM \_**</span><span class="sxs-lookup"><span data-stu-id="9cbc6-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





