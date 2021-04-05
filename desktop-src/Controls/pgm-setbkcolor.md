---
title: Mensagem de PGM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBkColor do pager.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Controles de PGM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085463"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="a445d-105">\_Mensagem SETBKCOLOR do PGM</span><span class="sxs-lookup"><span data-stu-id="a445d-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="a445d-106">Define a cor do plano de fundo atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="a445d-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="a445d-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="a445d-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a445d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a445d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a445d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a445d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a445d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a445d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a445d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a445d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a445d-112">Valor **COLORREF** que contém a nova cor de plano de fundo do controle de pager.</span><span class="sxs-lookup"><span data-stu-id="a445d-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a445d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a445d-113">Return value</span></span>

<span data-ttu-id="a445d-114">Retorna um valor **COLORREF** que contém a cor do plano de fundo anterior.</span><span class="sxs-lookup"><span data-stu-id="a445d-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="a445d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a445d-115">Remarks</span></span>

<span data-ttu-id="a445d-116">Por padrão, o controle de pager usará a cor de face do botão do sistema como a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="a445d-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="a445d-117">Essa é a mesma cor que pode ser recuperada chamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) com Color \_ btnface.</span><span class="sxs-lookup"><span data-stu-id="a445d-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a445d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a445d-118">Requirements</span></span>



| <span data-ttu-id="a445d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a445d-119">Requirement</span></span> | <span data-ttu-id="a445d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a445d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a445d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a445d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a445d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a445d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a445d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a445d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a445d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a445d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a445d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a445d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a445d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a445d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

