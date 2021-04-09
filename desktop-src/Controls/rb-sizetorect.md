---
title: Mensagem de RB_SIZETORECT (commctrl. h)
description: Tenta encontrar o melhor layout das faixas para o retângulo fornecido.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Controles de RB_SIZETORECT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086413"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="6951c-104">\_Mensagem SIZETORECT RB</span><span class="sxs-lookup"><span data-stu-id="6951c-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="6951c-105">Tenta encontrar o melhor layout das faixas para o retângulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="6951c-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="6951c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6951c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6951c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6951c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6951c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6951c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6951c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6951c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6951c-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica o retângulo para o qual o controle rebar deve ser dimensionado.</span><span class="sxs-lookup"><span data-stu-id="6951c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6951c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6951c-111">Return value</span></span>

<span data-ttu-id="6951c-112">Retornará um valor diferente de zero se ocorrer uma alteração de layout ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="6951c-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6951c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6951c-113">Remarks</span></span>

<span data-ttu-id="6951c-114">As bandas de rebar serão organizadas e encapsuladas conforme necessário para caber no retângulo.</span><span class="sxs-lookup"><span data-stu-id="6951c-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="6951c-115">As faixas que têm o \_ estilo RBBS VARIABLEHEIGHT serão redimensionadas de maneira uniforme possível para caber no retângulo.</span><span class="sxs-lookup"><span data-stu-id="6951c-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="6951c-116">A altura de um rebar horizontal ou a largura de um rebar vertical pode ser alterada, dependendo do novo layout.</span><span class="sxs-lookup"><span data-stu-id="6951c-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="6951c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6951c-117">Requirements</span></span>



| <span data-ttu-id="6951c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6951c-118">Requirement</span></span> | <span data-ttu-id="6951c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6951c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6951c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6951c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6951c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6951c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6951c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6951c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6951c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6951c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6951c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6951c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6951c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6951c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

