---
title: Mensagem de TTM_NEWTOOLRECT (commctrl. h)
description: Define um novo retângulo delimitador para uma ferramenta.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Controles de TTM_NEWTOOLRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455167"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="d5154-104">\_Mensagem TTM NEWTOOLRECT</span><span class="sxs-lookup"><span data-stu-id="d5154-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="d5154-105">Define um novo retângulo delimitador para uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d5154-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5154-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5154-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5154-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5154-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d5154-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d5154-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d5154-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5154-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5154-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d5154-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="d5154-111">Os membros de **HWND** e **UID** identificam uma ferramenta e o membro **Rect** especifica o novo retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="d5154-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="d5154-112">O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5154-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5154-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5154-113">Return value</span></span>

<span data-ttu-id="d5154-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d5154-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5154-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5154-115">Requirements</span></span>



| <span data-ttu-id="d5154-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5154-116">Requirement</span></span> | <span data-ttu-id="d5154-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d5154-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5154-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5154-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5154-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5154-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5154-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5154-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5154-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5154-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5154-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5154-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5154-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5154-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d5154-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d5154-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5154-125">**TTM \_ NEWTOOLRECTW** (Unicode) e **TTM \_ NEWTOOLRECTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5154-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





