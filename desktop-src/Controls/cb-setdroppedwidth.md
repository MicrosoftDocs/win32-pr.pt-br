---
title: Mensagem de CB_SETDROPPEDWIDTH (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETDROPPEDWIDTH para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Controles de CB_SETDROPPEDWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824402"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="e9ec8-104">\_Mensagem de SETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="e9ec8-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="e9ec8-105">Um aplicativo envia a mensagem **CB \_ SETDROPPEDWIDTH** para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e9ec8-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9ec8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ec8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ec8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9ec8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ec8-108">A largura mínima permitida da caixa de listagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e9ec8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9ec8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ec8-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ec8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9ec8-111">Return value</span></span>

<span data-ttu-id="e9ec8-112">Se a mensagem for bem-sucedida, o valor de retorno será a nova largura da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="e9ec8-113">Se a mensagem falhar, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ec8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ec8-114">Remarks</span></span>

<span data-ttu-id="e9ec8-115">Por padrão, a largura mínima permitida da caixa de listagem suspensa é zero.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="e9ec8-116">A largura da caixa de listagem é a largura mínima permitida ou a largura da caixa de combinação, o que for maior.</span><span class="sxs-lookup"><span data-stu-id="e9ec8-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ec8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ec8-117">Requirements</span></span>



| <span data-ttu-id="e9ec8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ec8-118">Requirement</span></span> | <span data-ttu-id="e9ec8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ec8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ec8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ec8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ec8-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9ec8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9ec8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ec8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ec8-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9ec8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9ec8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9ec8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ec8-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ec8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ec8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9ec8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ec8-127">**\_GETDROPPEDWIDTH CB**</span><span class="sxs-lookup"><span data-stu-id="e9ec8-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





