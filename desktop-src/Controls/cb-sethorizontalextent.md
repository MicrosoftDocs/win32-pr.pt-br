---
title: Mensagem de CB_SETHORIZONTALEXTENT (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETHORIZONTALEXTENT para definir a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Controles de CB_SETHORIZONTALEXTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455117"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="e5d81-104">\_Mensagem de SETHORIZONTALEXTENT CB</span><span class="sxs-lookup"><span data-stu-id="e5d81-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="e5d81-105">Um aplicativo envia a mensagem **CB \_ SETHORIZONTALEXTENT** para definir a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).</span><span class="sxs-lookup"><span data-stu-id="e5d81-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="e5d81-106">Se a largura da caixa de listagem for menor que esse valor, a barra de rolagem horizontal rolará horizontalmente os itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e5d81-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="e5d81-107">Se a largura da caixa de listagem for igual ou maior que esse valor, a barra de rolagem horizontal ficará oculta ou, se a caixa de combinação tiver o estilo [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e5d81-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5d81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5d81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d81-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5d81-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5d81-110">Especifica a largura rolável da caixa de listagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e5d81-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e5d81-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5d81-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5d81-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e5d81-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5d81-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d81-113">Requirements</span></span>



| <span data-ttu-id="e5d81-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d81-114">Requirement</span></span> | <span data-ttu-id="e5d81-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e5d81-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d81-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d81-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d81-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5d81-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5d81-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d81-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d81-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5d81-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5d81-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5d81-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d81-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5d81-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d81-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5d81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d81-123">**\_GETHORIZONTALEXTENT CB**</span><span class="sxs-lookup"><span data-stu-id="e5d81-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





