---
title: Mensagem de TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos que serão usados pelo controle da guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ setextendedattribute.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Controles de TCM_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009390"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="f5ccd-105">Mensagem do TCM \_ SETextendedattribute</span><span class="sxs-lookup"><span data-stu-id="f5ccd-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="f5ccd-106">Define os estilos estendidos que serão usados pelo controle da guia.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="f5ccd-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="f5ccd-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5ccd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ccd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ccd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5ccd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ccd-110">Um valor **DWORD** que indica quais estilos em *lParam* devem ser afetados.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="f5ccd-111">Somente os estilos estendidos em *wParam* serão alterados.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="f5ccd-112">Todos os outros estilos serão mantidos como estão.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="f5ccd-113">Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="f5ccd-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5ccd-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ccd-115">Valor que especifica os estilos de controle da guia estendida.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="f5ccd-116">Esse valor é uma combinação de [estilos estendidos](tab-control-extended-styles.md)de controle de guia.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ccd-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5ccd-117">Return value</span></span>

<span data-ttu-id="f5ccd-118">Retorna um valor **DWORD** que contém os estilos estendidos do controle de guia anterior.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ccd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ccd-119">Remarks</span></span>

<span data-ttu-id="f5ccd-120">O parâmetro *wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="f5ccd-121">Por exemplo, se você passar [**TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **TCS \_ ex \_ FLATSEPARATORS** será limpo, mas todos os outros estilos permanecerão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="f5ccd-122">Por motivos de compatibilidade com versões anteriores, a macro [**TabCtrl \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) não foi atualizada para usar *dwExMask*.</span><span class="sxs-lookup"><span data-stu-id="f5ccd-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ccd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ccd-123">Requirements</span></span>



| <span data-ttu-id="f5ccd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ccd-124">Requirement</span></span> | <span data-ttu-id="f5ccd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ccd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ccd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ccd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ccd-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5ccd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5ccd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ccd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ccd-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5ccd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5ccd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5ccd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ccd-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ccd-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ccd-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ccd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ccd-133">**TCM \_ GETextendedattribute**</span><span class="sxs-lookup"><span data-stu-id="f5ccd-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





