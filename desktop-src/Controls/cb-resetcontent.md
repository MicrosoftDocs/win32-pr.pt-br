---
title: Mensagem de CB_RESETCONTENT (WinUser. h)
description: Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Controles de CB_RESETCONTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824404"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="bed1b-104">\_Mensagem de RESETCONTENT CB</span><span class="sxs-lookup"><span data-stu-id="bed1b-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="bed1b-105">Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="bed1b-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="bed1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bed1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed1b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bed1b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bed1b-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bed1b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bed1b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bed1b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bed1b-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bed1b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed1b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bed1b-111">Return value</span></span>

<span data-ttu-id="bed1b-112">Essa mensagem sempre retorna CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bed1b-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bed1b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bed1b-113">Remarks</span></span>

<span data-ttu-id="bed1b-114">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o proprietário da caixa de combinação receberá uma mensagem [**\_ DELETEITEM do WM**](wm-deleteitem.md) para cada item na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="bed1b-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed1b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bed1b-115">Requirements</span></span>



| <span data-ttu-id="bed1b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bed1b-116">Requirement</span></span> | <span data-ttu-id="bed1b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bed1b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed1b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bed1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bed1b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bed1b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bed1b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bed1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bed1b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bed1b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bed1b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bed1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed1b-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bed1b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed1b-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bed1b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bed1b-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bed1b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bed1b-126">**excluído de CB \_**</span><span class="sxs-lookup"><span data-stu-id="bed1b-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="bed1b-127">**DELETEITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bed1b-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





