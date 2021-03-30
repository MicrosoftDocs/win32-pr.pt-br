---
title: Mensagem de LB_GETITEMRECT (WinUser. h)
description: Obtém as dimensões do retângulo que vincula um item da caixa de listagem, como é exibido atualmente na caixa de listagem.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- Controles de LB_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455012"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="eb3a5-104">GETITEMRECT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="eb3a5-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="eb3a5-105">Obtém as dimensões do retângulo que vincula um item da caixa de listagem, como é exibido atualmente na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb3a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb3a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3a5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb3a5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb3a5-108">O índice de base zero do item.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-108">The zero-based index of the item.</span></span>

<span data-ttu-id="eb3a5-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="eb3a5-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="eb3a5-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="eb3a5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb3a5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb3a5-113">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as coordenadas do cliente para o item na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="eb3a5-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3a5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb3a5-114">Return value</span></span>

<span data-ttu-id="eb3a5-115">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="eb3a5-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3a5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3a5-116">Requirements</span></span>



| <span data-ttu-id="eb3a5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3a5-117">Requirement</span></span> | <span data-ttu-id="eb3a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3a5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3a5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb3a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3a5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb3a5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb3a5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb3a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3a5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb3a5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb3a5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb3a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb3a5-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3a5-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3a5-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eb3a5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb3a5-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb3a5-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

