---
title: Mensagem de TCM_SETITEM (commctrl. h)
description: Define alguns ou todos os atributos de uma guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Controles de TCM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644246"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="db0a5-105">\_Mensagem SETITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="db0a5-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="db0a5-106">Define alguns ou todos os atributos de uma guia.</span><span class="sxs-lookup"><span data-stu-id="db0a5-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="db0a5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .</span><span class="sxs-lookup"><span data-stu-id="db0a5-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db0a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db0a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db0a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db0a5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db0a5-110">Índice do item.</span><span class="sxs-lookup"><span data-stu-id="db0a5-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="db0a5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db0a5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db0a5-112">Ponteiro para uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contém os novos atributos de item.</span><span class="sxs-lookup"><span data-stu-id="db0a5-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="db0a5-113">O membro **Mask** especifica quais atributos definir.</span><span class="sxs-lookup"><span data-stu-id="db0a5-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="db0a5-114">Se o membro de **máscara** especificar o \_ valor de texto TCIF, o membro **pszText** será o endereço de uma cadeia de caracteres terminada em nulo e o membro **cchTextMax** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="db0a5-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db0a5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db0a5-115">Return value</span></span>

<span data-ttu-id="db0a5-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="db0a5-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="db0a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db0a5-117">Requirements</span></span>



| <span data-ttu-id="db0a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db0a5-118">Requirement</span></span> | <span data-ttu-id="db0a5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="db0a5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db0a5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db0a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db0a5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db0a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db0a5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db0a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db0a5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db0a5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db0a5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db0a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db0a5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db0a5-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db0a5-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="db0a5-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db0a5-127">**TCM \_ SETITEMW** (Unicode) e **TCM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db0a5-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





