---
title: Mensagem de BCM_GETSPLITINFO (commctrl. h)
description: Obtém informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o botão \_ GetSplitInfo macro.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Controles de BCM_GETSPLITINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918525"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="55d2c-105">\_Mensagem GETSPLITINFO do BCM</span><span class="sxs-lookup"><span data-stu-id="55d2c-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="55d2c-106">Obtém informações para um controle de botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="55d2c-106">Gets information for a split button control.</span></span> <span data-ttu-id="55d2c-107">Envie essa mensagem explicitamente ou usando o [**botão \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span><span class="sxs-lookup"><span data-stu-id="55d2c-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="55d2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55d2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d2c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55d2c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55d2c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="55d2c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55d2c-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="55d2c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55d2c-112">Um ponteiro para uma estrutura de [**\_ SPLITINFO de botão**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) para receber informações sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="55d2c-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="55d2c-113">O chamador é responsável por alocar a memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="55d2c-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="55d2c-114">Defina o membro de **máscara** desta estrutura para determinar quais informações receber.</span><span class="sxs-lookup"><span data-stu-id="55d2c-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d2c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55d2c-115">Return value</span></span>

<span data-ttu-id="55d2c-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="55d2c-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d2c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="55d2c-117">Remarks</span></span>

<span data-ttu-id="55d2c-118">Use esta mensagem somente com os estilos de botão [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="55d2c-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d2c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55d2c-119">Requirements</span></span>



| <span data-ttu-id="55d2c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d2c-120">Requirement</span></span> | <span data-ttu-id="55d2c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="55d2c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55d2c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55d2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55d2c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55d2c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55d2c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55d2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55d2c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55d2c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55d2c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55d2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d2c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d2c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d2c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="55d2c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="55d2c-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="55d2c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55d2c-130">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="55d2c-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="55d2c-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="55d2c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55d2c-132">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="55d2c-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





