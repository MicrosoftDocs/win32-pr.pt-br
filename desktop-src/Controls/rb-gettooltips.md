---
title: Mensagem de RB_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para qualquer controle ToolTip associado ao controle rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- Controles de RB_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085808"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="6bd51-104">\_Mensagem RB GETtooltips</span><span class="sxs-lookup"><span data-stu-id="6bd51-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="6bd51-105">Recupera o identificador para qualquer controle ToolTip associado ao controle rebar.</span><span class="sxs-lookup"><span data-stu-id="6bd51-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bd51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bd51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd51-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bd51-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6bd51-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6bd51-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6bd51-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bd51-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6bd51-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6bd51-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd51-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bd51-111">Return value</span></span>

<span data-ttu-id="6bd51-112">Retorna um valor **HWND** que é o identificador para o controle ToolTip associado ao controle rebar ou zero se nenhum controle ToolTip estiver associado ao controle rebar.</span><span class="sxs-lookup"><span data-stu-id="6bd51-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd51-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bd51-113">Requirements</span></span>



| <span data-ttu-id="6bd51-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bd51-114">Requirement</span></span> | <span data-ttu-id="6bd51-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6bd51-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd51-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bd51-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd51-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bd51-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bd51-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bd51-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd51-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6bd51-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bd51-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bd51-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bd51-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bd51-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





