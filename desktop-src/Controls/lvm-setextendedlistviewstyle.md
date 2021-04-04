---
title: Mensagem de LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Define estilos estendidos em controles de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetExtendedListViewStyle ou ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Controles de LVM_SETEXTENDEDLISTVIEWSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917994"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="bc659-105">\_Mensagem SETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="bc659-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="bc659-106">Define estilos estendidos em controles de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="bc659-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="bc659-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) ou [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="bc659-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc659-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc659-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc659-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc659-110">Valor **DWORD** que especifica quais estilos em *lParam* devem ser afetados.</span><span class="sxs-lookup"><span data-stu-id="bc659-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="bc659-111">Esse parâmetro pode ser uma combinação de [**estilos de List-View estendidos**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="bc659-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="bc659-112">Somente os estilos estendidos em *wParam* serão alterados.</span><span class="sxs-lookup"><span data-stu-id="bc659-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="bc659-113">Todos os outros estilos serão mantidos como estão.</span><span class="sxs-lookup"><span data-stu-id="bc659-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="bc659-114">Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.</span><span class="sxs-lookup"><span data-stu-id="bc659-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="bc659-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc659-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc659-116">Valor **DWORD** que especifica os estilos de controle de exibição de lista estendida a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="bc659-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="bc659-117">Esse parâmetro pode ser uma combinação de [**estilos de List-View estendidos**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="bc659-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="bc659-118">Os estilos que não estão definidos, mas que são especificados em *wParam*, são removidos.</span><span class="sxs-lookup"><span data-stu-id="bc659-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc659-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc659-119">Return value</span></span>

<span data-ttu-id="bc659-120">Retorna um valor **DWORD** que contém os estilos de controle de exibição de lista estendida anteriores.</span><span class="sxs-lookup"><span data-stu-id="bc659-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc659-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc659-121">Remarks</span></span>

<span data-ttu-id="bc659-122">O parâmetro *wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro.</span><span class="sxs-lookup"><span data-stu-id="bc659-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="bc659-123">Por exemplo, se você passar [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* e 0 para *lParam*, o estilo **LVS \_ ex \_ FULLROWSELECT** será limpo, mas todos os outros estilos permanecerão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="bc659-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="bc659-124">Por motivos de compatibilidade com versões anteriores, a macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) não foi atualizada para usar *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bc659-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="bc659-125">Para usar o valor *wParam* , use a macro [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="bc659-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="bc659-126">Quando você usa essa mensagem para definir o estilo de [**\_ caixas de \_ seleção LVS ex**](extended-list-view-styles.md) , qualquer índice de imagem de estado definido anteriormente será Descartado.</span><span class="sxs-lookup"><span data-stu-id="bc659-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="bc659-127">Todas as caixas de seleção serão inicializadas para o estado desmarcado.</span><span class="sxs-lookup"><span data-stu-id="bc659-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="bc659-128">O índice de imagem de estado está contido em bits 12 a 15 do membro de **estado** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="bc659-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc659-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc659-129">Requirements</span></span>



| <span data-ttu-id="bc659-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc659-130">Requirement</span></span> | <span data-ttu-id="bc659-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bc659-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc659-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc659-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc659-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc659-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc659-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc659-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc659-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bc659-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc659-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc659-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc659-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc659-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





