---
title: Mensagem de PGM_GETDROPTARGET (commctrl. h)
description: Recupera o ponteiro de interface IDropTarget de um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetDropTarget do pager.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Controles de PGM_GETDROPTARGET de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455540"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="637ae-105">\_Mensagem GETDROPTARGET do PGM</span><span class="sxs-lookup"><span data-stu-id="637ae-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="637ae-106">Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de pager.</span><span class="sxs-lookup"><span data-stu-id="637ae-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="637ae-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetDropTarget do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="637ae-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="637ae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="637ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="637ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="637ae-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="637ae-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="637ae-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="637ae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="637ae-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="637ae-112">Ponteiro para um ponteiro [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recebe o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="637ae-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="637ae-113">É responsabilidade do chamador chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) neste ponteiro quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="637ae-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="637ae-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="637ae-114">Return value</span></span>

<span data-ttu-id="637ae-115">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="637ae-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="637ae-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637ae-116">Requirements</span></span>



| <span data-ttu-id="637ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="637ae-117">Requirement</span></span> | <span data-ttu-id="637ae-118">Valor</span><span class="sxs-lookup"><span data-stu-id="637ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="637ae-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="637ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="637ae-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="637ae-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="637ae-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="637ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="637ae-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="637ae-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="637ae-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="637ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="637ae-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="637ae-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

