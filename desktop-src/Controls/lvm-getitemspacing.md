---
title: Mensagem de LVM_GETITEMSPACING (commctrl. h)
description: Determina o espaçamento entre os itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemSpacing do ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Controles de LVM_GETITEMSPACING de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918971"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="79de4-105">\_Mensagem GETITEMSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="79de4-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="79de4-106">Determina o espaçamento entre os itens em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="79de4-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="79de4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemSpacing do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .</span><span class="sxs-lookup"><span data-stu-id="79de4-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79de4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79de4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79de4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79de4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79de4-110">Exibição para a qual recuperar o espaçamento do item.</span><span class="sxs-lookup"><span data-stu-id="79de4-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="79de4-111">Esse parâmetro é **verdadeiro** para exibição de ícone pequeno ou **falso** para exibição de ícone.</span><span class="sxs-lookup"><span data-stu-id="79de4-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="79de4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79de4-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="79de4-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="79de4-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79de4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79de4-114">Return value</span></span>

<span data-ttu-id="79de4-115">Retorna a quantidade de espaçamento entre os itens.</span><span class="sxs-lookup"><span data-stu-id="79de4-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="79de4-116">O espaçamento horizontal está contido no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o espaçamento vertical está contido no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79de4-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="79de4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79de4-117">Requirements</span></span>



| <span data-ttu-id="79de4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="79de4-118">Requirement</span></span> | <span data-ttu-id="79de4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="79de4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79de4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79de4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79de4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79de4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79de4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79de4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79de4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79de4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79de4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79de4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79de4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79de4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

