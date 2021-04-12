---
title: Mensagem de LVM_GETSTRINGWIDTH (commctrl. h)
description: Determina a largura de uma cadeia de caracteres especificada usando a fonte atual do controle de exibição de lista especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetStringWidth do ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Controles de LVM_GETSTRINGWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499666"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="c2614-105">\_Mensagem GETSTRINGWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="c2614-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="c2614-106">Determina a largura de uma cadeia de caracteres especificada usando a fonte atual do controle de exibição de lista especificado.</span><span class="sxs-lookup"><span data-stu-id="c2614-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="c2614-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetStringWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .</span><span class="sxs-lookup"><span data-stu-id="c2614-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2614-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2614-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2614-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2614-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2614-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2614-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2614-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2614-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2614-112">Ponteiro para uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c2614-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2614-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2614-113">Return value</span></span>

<span data-ttu-id="c2614-114">Retorna a largura da cadeia de caracteres se for bem-sucedida ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c2614-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2614-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2614-115">Remarks</span></span>

<span data-ttu-id="c2614-116">A \_ mensagem LVM GETSTRINGWIDTH retorna a largura exata, em pixels, da cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="c2614-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="c2614-117">Se você usar a largura da cadeia de caracteres retornada como a largura da coluna na mensagem [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , a cadeia de caracteres será truncada.</span><span class="sxs-lookup"><span data-stu-id="c2614-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="c2614-118">Para recuperar a largura da coluna que pode conter a cadeia de caracteres sem truncar, você deve adicionar o preenchimento à largura da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="c2614-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2614-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2614-119">Requirements</span></span>



| <span data-ttu-id="c2614-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2614-120">Requirement</span></span> | <span data-ttu-id="c2614-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c2614-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2614-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2614-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2614-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2614-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2614-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2614-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2614-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2614-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2614-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2614-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2614-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2614-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c2614-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c2614-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c2614-129">**LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c2614-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





