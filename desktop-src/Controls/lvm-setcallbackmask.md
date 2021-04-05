---
title: Mensagem de LVM_SETCALLBACKMASK (commctrl. h)
description: Altera a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetCallbackMask do ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Controles de LVM_SETCALLBACKMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085405"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="3741f-105">\_Mensagem SETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="3741f-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="3741f-106">Altera a máscara de retorno de chamada para um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="3741f-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="3741f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetCallbackMask do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="3741f-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3741f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3741f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3741f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3741f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3741f-110">Valor da máscara de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="3741f-110">Value of the callback mask.</span></span> <span data-ttu-id="3741f-111">Os bits da máscara indicam os Estados do item ou as imagens para as quais o aplicativo armazena os dados de estado atuais.</span><span class="sxs-lookup"><span data-stu-id="3741f-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="3741f-112">Esse valor pode ser qualquer combinação das seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="3741f-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="3741f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3741f-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="3741f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3741f-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="3741f-115"><dt>**LVIS \_ recortar**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="3741f-116">O item é marcado para uma operação de recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="3741f-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="3741f-117"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="3741f-118">O item é realçado como um destino do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="3741f-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="3741f-119"><dt>**LVIS com \_ foco**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="3741f-120">O item tem o foco.</span><span class="sxs-lookup"><span data-stu-id="3741f-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="3741f-121"><dt>**LVIS \_ selecionado**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="3741f-122">O item está selecionado.</span><span class="sxs-lookup"><span data-stu-id="3741f-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="3741f-123"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="3741f-124">O aplicativo armazena o índice da lista de imagens da imagem de sobreposição atual para cada item.</span><span class="sxs-lookup"><span data-stu-id="3741f-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="3741f-125"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="3741f-126">O aplicativo armazena o índice da lista de imagens da imagem de estado atual para cada item.</span><span class="sxs-lookup"><span data-stu-id="3741f-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="3741f-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3741f-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3741f-128">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3741f-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3741f-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3741f-129">Return value</span></span>

<span data-ttu-id="3741f-130">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3741f-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3741f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="3741f-131">Remarks</span></span>

<span data-ttu-id="3741f-132">A *máscara de retorno de chamada* de um controle de exibição de lista é um conjunto de sinalizadores de bits que especificam os Estados de item para os quais o aplicativo, em vez do controle, armazena os dados atuais.</span><span class="sxs-lookup"><span data-stu-id="3741f-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="3741f-133">A máscara de retorno de chamada aplica-se a todos os itens do controle, diferentemente da designação do item de retorno de chamada, que se aplica a um item específico.</span><span class="sxs-lookup"><span data-stu-id="3741f-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="3741f-134">A máscara de retorno de chamada é zero por padrão, o que significa que o controle List-View armazena todas as informações de estado do item.</span><span class="sxs-lookup"><span data-stu-id="3741f-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="3741f-135">Depois de criar um controle de exibição de lista e inicializar seus itens, você pode enviar a mensagem **LVM \_ SETCALLBACKMASK** para alterar a máscara de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="3741f-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="3741f-136">Para recuperar a máscara de retorno de chamada atual, envie a mensagem [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="3741f-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="3741f-137">Para obter mais informações sobre imagens de sobreposição e imagens de estado, consulte [adicionando List-View listas](using-list-view-controls.md)de imagens.</span><span class="sxs-lookup"><span data-stu-id="3741f-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="3741f-138">Para obter mais informações sobre retornos de chamada de exibição de lista, consulte [itens de retorno de chamada e a máscara de retorno de chamada](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3741f-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3741f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3741f-139">Requirements</span></span>



| <span data-ttu-id="3741f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3741f-140">Requirement</span></span> | <span data-ttu-id="3741f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3741f-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3741f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3741f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3741f-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3741f-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3741f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3741f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3741f-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3741f-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3741f-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3741f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3741f-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3741f-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3741f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="3741f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3741f-149">**LVN \_ GETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="3741f-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





