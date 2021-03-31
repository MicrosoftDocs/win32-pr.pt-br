---
title: Mensagem de PGM_GETBKCOLOR (commctrl. h)
description: Recupera a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBkColor do pager.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Controles de PGM_GETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644906"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="4e2bc-105">\_Mensagem GETBKCOLOR do PGM</span><span class="sxs-lookup"><span data-stu-id="4e2bc-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="4e2bc-106">Recupera a cor do plano de fundo atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="4e2bc-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="4e2bc-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e2bc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e2bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e2bc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4e2bc-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4e2bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e2bc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e2bc-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2bc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e2bc-113">Return value</span></span>

<span data-ttu-id="4e2bc-114">Retorna um valor **COLORREF** que contém a cor do plano de fundo atual.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2bc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e2bc-115">Remarks</span></span>

<span data-ttu-id="4e2bc-116">Por padrão, o controle de pager usará a cor de face do botão do sistema como a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="4e2bc-117">Essa é a mesma cor que pode ser recuperada chamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) com Color \_ btnface.</span><span class="sxs-lookup"><span data-stu-id="4e2bc-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e2bc-118">Requirements</span></span>



| <span data-ttu-id="4e2bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2bc-119">Requirement</span></span> | <span data-ttu-id="4e2bc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4e2bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2bc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2bc-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e2bc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e2bc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2bc-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e2bc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e2bc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e2bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2bc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2bc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

