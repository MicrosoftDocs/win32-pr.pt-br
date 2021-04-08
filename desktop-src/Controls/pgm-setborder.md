---
title: Mensagem de PGM_SETBORDER (commctrl. h)
description: Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBorder do pager.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Controles de PGM_SETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009264"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="dc7ec-105">\_Mensagem de SETborder do PGM</span><span class="sxs-lookup"><span data-stu-id="dc7ec-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="dc7ec-106">Define o tamanho da borda atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="dc7ec-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .</span><span class="sxs-lookup"><span data-stu-id="dc7ec-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc7ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc7ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc7ec-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc7ec-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc7ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc7ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc7ec-112">Novo tamanho da borda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-112">New size of the border, in pixels.</span></span> <span data-ttu-id="dc7ec-113">Esse valor não deve ser maior que o botão de pager ou menor que zero.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="dc7ec-114">Se *lParam* for muito grande, a borda será desenhada com o mesmo tamanho do botão.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="dc7ec-115">Se *lParam* for negativo, o tamanho da borda será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7ec-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc7ec-116">Return value</span></span>

<span data-ttu-id="dc7ec-117">Retorna um valor INT que contém o tamanho da borda anterior, em pixels.</span><span class="sxs-lookup"><span data-stu-id="dc7ec-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc7ec-118">Requirements</span></span>



| <span data-ttu-id="dc7ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc7ec-119">Requirement</span></span> | <span data-ttu-id="dc7ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dc7ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7ec-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc7ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7ec-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc7ec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc7ec-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc7ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7ec-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc7ec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc7ec-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc7ec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc7ec-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc7ec-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





