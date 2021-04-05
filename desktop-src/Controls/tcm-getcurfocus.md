---
title: Mensagem de TCM_GETCURFOCUS (commctrl. h)
description: Retorna o índice do item que tem o foco em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- Controles de TCM_GETCURFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919021"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="7d910-105">\_Mensagem GETCURFOCUS de TCM</span><span class="sxs-lookup"><span data-stu-id="7d910-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="7d910-106">Retorna o índice do item que tem o foco em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="7d910-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="7d910-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="7d910-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d910-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d910-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d910-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7d910-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7d910-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7d910-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d910-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7d910-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7d910-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d910-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d910-113">Return value</span></span>

<span data-ttu-id="7d910-114">Retorna o índice do item de guia que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="7d910-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d910-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d910-115">Remarks</span></span>

<span data-ttu-id="7d910-116">O item que tem o foco pode ser diferente do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="7d910-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d910-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d910-117">Requirements</span></span>



| <span data-ttu-id="7d910-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d910-118">Requirement</span></span> | <span data-ttu-id="7d910-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7d910-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d910-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d910-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d910-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d910-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d910-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d910-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d910-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d910-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d910-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d910-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d910-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d910-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





