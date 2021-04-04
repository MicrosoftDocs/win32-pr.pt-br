---
title: Mensagem de LVM_SETITEMPOSITION (commctrl. h)
description: Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno). Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemPosition do ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Controles de LVM_SETITEMPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824455"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="bb78a-105">\_Mensagem SETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="bb78a-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="bb78a-106">Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno).</span><span class="sxs-lookup"><span data-stu-id="bb78a-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="bb78a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemPosition do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .</span><span class="sxs-lookup"><span data-stu-id="bb78a-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb78a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb78a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb78a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb78a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb78a-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="bb78a-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="bb78a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb78a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb78a-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a nova posição x do canto superior esquerdo do item, em coordenadas de exibição.</span><span class="sxs-lookup"><span data-stu-id="bb78a-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="bb78a-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a nova posição y do canto superior esquerdo do item, em coordenadas de exibição.</span><span class="sxs-lookup"><span data-stu-id="bb78a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb78a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb78a-114">Return value</span></span>

<span data-ttu-id="bb78a-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bb78a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb78a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb78a-116">Remarks</span></span>

<span data-ttu-id="bb78a-117">Se o controle de exibição de lista tiver o estilo de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) , os itens no controle de exibição de lista serão organizados depois que a posição do item for definida.</span><span class="sxs-lookup"><span data-stu-id="bb78a-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="bb78a-118">No Windows Vista, o envio dessa mensagem para um controle de exibição de lista com o estilo [**\_ AutoOrganizar LVS**](list-view-window-styles.md) não faz nada e o valor de retorno é **false**.</span><span class="sxs-lookup"><span data-stu-id="bb78a-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb78a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb78a-119">Requirements</span></span>



| <span data-ttu-id="bb78a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb78a-120">Requirement</span></span> | <span data-ttu-id="bb78a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bb78a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb78a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb78a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb78a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb78a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb78a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb78a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb78a-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb78a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb78a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb78a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb78a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb78a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

