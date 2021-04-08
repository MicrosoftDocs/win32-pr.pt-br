---
title: Mensagem de CB_GETMINVISIBLE (commctrl. h)
description: Obtém o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Controles de CB_GETMINVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824405"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="6b90a-104">\_Mensagem de GETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="6b90a-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="6b90a-105">Obtém o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6b90a-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b90a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b90a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b90a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b90a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b90a-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6b90a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b90a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b90a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b90a-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6b90a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b90a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b90a-111">Return value</span></span>

<span data-ttu-id="6b90a-112">O valor de retorno é o número mínimo de itens visíveis.</span><span class="sxs-lookup"><span data-stu-id="6b90a-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b90a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b90a-113">Remarks</span></span>

<span data-ttu-id="6b90a-114">Quando o número de itens na lista suspensa for maior que o mínimo, a caixa de combinação usará uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="6b90a-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="6b90a-115">Essa mensagem será ignorada se o controle da caixa de combinação tiver o estilo [**\_ NOINTEGRALHEIGHT CBS**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6b90a-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="6b90a-116">Para usar **CB \_ GETMINVISIBLE**, o aplicativo deve especificar comctl32.dll versão 6 no manifesto.</span><span class="sxs-lookup"><span data-stu-id="6b90a-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="6b90a-117">Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b90a-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b90a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b90a-118">Requirements</span></span>



| <span data-ttu-id="6b90a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b90a-119">Requirement</span></span> | <span data-ttu-id="6b90a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6b90a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b90a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b90a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b90a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b90a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b90a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b90a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b90a-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b90a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b90a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b90a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b90a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b90a-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b90a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b90a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b90a-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6b90a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b90a-129">**\_SETMINVISIBLE CB**</span><span class="sxs-lookup"><span data-stu-id="6b90a-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="6b90a-130">**GetMinVisible da ComboBox \_**</span><span class="sxs-lookup"><span data-stu-id="6b90a-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





