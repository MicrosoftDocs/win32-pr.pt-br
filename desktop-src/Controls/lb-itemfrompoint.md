---
title: Mensagem de LB_ITEMFROMPOINT (WinUser. h)
description: Obtém o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Controles de LB_ITEMFROMPOINT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645030"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="c8408-104">ITEMFROMPOINT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="c8408-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="c8408-105">Obtém o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="c8408-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8408-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8408-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8408-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8408-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c8408-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c8408-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8408-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8408-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a coordenada x de um ponto, em relação ao canto superior esquerdo da área do cliente da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="c8408-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="c8408-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a coordenada y de um ponto, em relação ao canto superior esquerdo da área do cliente da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="c8408-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8408-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8408-112">Return value</span></span>

<span data-ttu-id="c8408-113">O valor de retorno contém o índice do item mais próximo no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8408-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="c8408-114">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) será zero se o ponto especificado estiver na área do cliente da caixa de listagem, ou um se estiver fora da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="c8408-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8408-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8408-115">Requirements</span></span>



| <span data-ttu-id="c8408-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8408-116">Requirement</span></span> | <span data-ttu-id="c8408-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c8408-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8408-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8408-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8408-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8408-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8408-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8408-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8408-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8408-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8408-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8408-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8408-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8408-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8408-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c8408-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8408-125">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="c8408-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

