---
title: Mensagem de CB_SETMINVISIBLE (commctrl. h)
description: Um aplicativo envia uma \_ mensagem de SETMINVISIBLE CB para definir o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Controles de CB_SETMINVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085216"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="1a6ac-104">\_Mensagem de SETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="1a6ac-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="1a6ac-105">Um aplicativo envia uma mensagem de **\_ SETMINVISIBLE CB** para definir o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a6ac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a6ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a6ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6ac-108">Especifica o número mínimo de itens visíveis.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="1a6ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a6ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6ac-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6ac-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a6ac-111">Return value</span></span>

<span data-ttu-id="1a6ac-112">Se a mensagem for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="1a6ac-113">Caso contrário, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6ac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a6ac-114">Remarks</span></span>

<span data-ttu-id="1a6ac-115">Quando o número de itens na lista suspensa for maior que o mínimo, a caixa de combinação usará uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="1a6ac-116">Por padrão, 30 é o número mínimo de itens visíveis.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="1a6ac-117">Essa mensagem será ignorada se o controle da caixa de combinação tiver o estilo [**\_ NOINTEGRALHEIGHT CBS**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="1a6ac-118">Para usar **CB \_ SETMINVISIBLE**, o aplicativo deve especificar comctl32.dll versão 6 no manifesto.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="1a6ac-119">Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6ac-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a6ac-120">Requirements</span></span>



| <span data-ttu-id="1a6ac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a6ac-121">Requirement</span></span> | <span data-ttu-id="1a6ac-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a6ac-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6ac-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6ac-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a6ac-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a6ac-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6ac-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a6ac-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a6ac-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a6ac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6ac-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ac-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6ac-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a6ac-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a6ac-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1a6ac-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a6ac-131">**\_GETMINVISIBLE CB**</span><span class="sxs-lookup"><span data-stu-id="1a6ac-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="1a6ac-132">**SetMinVisible da ComboBox \_**</span><span class="sxs-lookup"><span data-stu-id="1a6ac-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





