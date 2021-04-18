---
title: Mensagem de BCM_SETSPLITINFO (commctrl. h)
description: Define informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o botão \_ SetSplitInfo macro.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Controles de BCM_SETSPLITINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753577"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="fd612-105">\_Mensagem SETSPLITINFO do BCM</span><span class="sxs-lookup"><span data-stu-id="fd612-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="fd612-106">Define informações para um controle de botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="fd612-106">Sets information for a split button control.</span></span> <span data-ttu-id="fd612-107">Envie essa mensagem explicitamente ou usando o [**botão \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span><span class="sxs-lookup"><span data-stu-id="fd612-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd612-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd612-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd612-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd612-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd612-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fd612-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd612-111">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd612-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd612-112">Um ponteiro para uma estrutura de [**\_ SPLITINFO de botão**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) que contém informações sobre o botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="fd612-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd612-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd612-113">Return value</span></span>

<span data-ttu-id="fd612-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fd612-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd612-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd612-115">Remarks</span></span>

<span data-ttu-id="fd612-116">Use esta mensagem somente com os estilos de botão [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fd612-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd612-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd612-117">Requirements</span></span>



| <span data-ttu-id="fd612-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd612-118">Requirement</span></span> | <span data-ttu-id="fd612-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fd612-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd612-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd612-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd612-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd612-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd612-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd612-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd612-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd612-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd612-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd612-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd612-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd612-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd612-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd612-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd612-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fd612-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fd612-128">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="fd612-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="fd612-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="fd612-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fd612-130">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="fd612-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





