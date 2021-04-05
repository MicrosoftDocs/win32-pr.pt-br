---
title: Mensagem de CB_GETDROPPEDWIDTH (WinUser. h)
description: Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Controles de CB_GETDROPPEDWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009366"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="dd4bb-104">\_Mensagem de GETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="dd4bb-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="dd4bb-105">Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="dd4bb-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd4bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd4bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd4bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd4bb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd4bb-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dd4bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd4bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd4bb-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd4bb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd4bb-111">Return value</span></span>

<span data-ttu-id="dd4bb-112">Se a mensagem tiver sucesso, o valor de retorno será a largura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="dd4bb-113">Se a mensagem falhar, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd4bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd4bb-114">Remarks</span></span>

<span data-ttu-id="dd4bb-115">Por padrão, a largura mínima permitida da caixa de listagem suspensa é zero.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="dd4bb-116">A largura da caixa de listagem é a largura mínima permitida ou a largura da caixa de combinação, o que for maior.</span><span class="sxs-lookup"><span data-stu-id="dd4bb-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd4bb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd4bb-117">Requirements</span></span>



| <span data-ttu-id="dd4bb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd4bb-118">Requirement</span></span> | <span data-ttu-id="dd4bb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dd4bb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4bb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd4bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4bb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd4bb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dd4bb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd4bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4bb-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd4bb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dd4bb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd4bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd4bb-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd4bb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4bb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd4bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4bb-127">**\_SETDROPPEDWIDTH CB**</span><span class="sxs-lookup"><span data-stu-id="dd4bb-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





