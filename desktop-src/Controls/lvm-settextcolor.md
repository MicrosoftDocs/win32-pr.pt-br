---
title: Mensagem de LVM_SETTEXTCOLOR (commctrl. h)
description: Define a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTextColor do ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Controles de LVM_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085401"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="fba87-105">\_Mensagem SETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="fba87-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="fba87-106">Define a cor do texto de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="fba87-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="fba87-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTextColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="fba87-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fba87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fba87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fba87-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fba87-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fba87-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fba87-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fba87-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fba87-112">Um [**COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor do texto.</span><span class="sxs-lookup"><span data-stu-id="fba87-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba87-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fba87-113">Return value</span></span>

<span data-ttu-id="fba87-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fba87-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba87-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba87-115">Requirements</span></span>



| <span data-ttu-id="fba87-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba87-116">Requirement</span></span> | <span data-ttu-id="fba87-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fba87-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fba87-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fba87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fba87-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fba87-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fba87-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fba87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fba87-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fba87-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fba87-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fba87-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fba87-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba87-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

