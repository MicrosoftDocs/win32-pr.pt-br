---
title: Mensagem de TCM_HIGHLIGHTITEM (commctrl. h)
description: Define o estado de realce de um item de guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Controles de TCM_HIGHLIGHTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824708"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="b3a9e-105">\_Mensagem HIGHLIGHTITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="b3a9e-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="b3a9e-106">Define o estado de realce de um item de guia.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="b3a9e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .</span><span class="sxs-lookup"><span data-stu-id="b3a9e-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3a9e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3a9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a9e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3a9e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a9e-110">Um valor **int** que especifica o índice de base zero de um item de controle de guia.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="b3a9e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3a9e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a9e-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que especifica o estado de realce a ser definido.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="b3a9e-113">Se esse valor for **true**, a guia será realçada; Se for **false**, a guia será definida como seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="b3a9e-114">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a9e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3a9e-115">Return value</span></span>

<span data-ttu-id="b3a9e-116">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a9e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3a9e-117">Remarks</span></span>

<span data-ttu-id="b3a9e-118">No Comctl32.dll versão 6,0, essa mensagem não tem efeito visível quando um tema está ativo.</span><span class="sxs-lookup"><span data-stu-id="b3a9e-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a9e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3a9e-119">Requirements</span></span>



| <span data-ttu-id="b3a9e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a9e-120">Requirement</span></span> | <span data-ttu-id="b3a9e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b3a9e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a9e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3a9e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a9e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3a9e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3a9e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3a9e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a9e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3a9e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3a9e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3a9e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3a9e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a9e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

