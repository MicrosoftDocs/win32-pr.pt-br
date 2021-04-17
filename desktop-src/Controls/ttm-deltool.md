---
title: Mensagem de TTM_DELTOOL (commctrl. h)
description: Remove uma ferramenta de um controle ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Controles de TTM_DELTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754801"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="0e779-104">\_Mensagem TTM DELTOOL</span><span class="sxs-lookup"><span data-stu-id="0e779-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="0e779-105">Remove uma ferramenta de um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="0e779-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e779-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e779-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e779-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e779-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e779-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0e779-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e779-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e779-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e779-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="0e779-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="0e779-111">Os membros de **HWND** e **UID** identificam a ferramenta a ser removida e o membro **cbSize** deve especificar o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="0e779-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="0e779-112">Todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="0e779-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e779-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e779-113">Return value</span></span>

<span data-ttu-id="0e779-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0e779-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e779-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e779-115">Requirements</span></span>



| <span data-ttu-id="0e779-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e779-116">Requirement</span></span> | <span data-ttu-id="0e779-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0e779-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e779-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e779-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e779-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e779-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e779-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e779-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e779-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e779-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e779-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e779-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e779-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e779-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0e779-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0e779-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e779-125">**TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e779-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="0e779-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e779-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e779-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0e779-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e779-128">**addferramenta TTM \_**</span><span class="sxs-lookup"><span data-stu-id="0e779-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="0e779-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0e779-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e779-130">Sobre os controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="0e779-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





