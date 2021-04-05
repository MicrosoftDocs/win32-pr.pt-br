---
title: Mensagem de PBM_GETBKCOLOR (commctrl. h)
description: Obtém a cor do plano de fundo da barra de progresso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Controles de PBM_GETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824588"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="077d5-104">Mensagem do GETBKCOLOR do PBM \_</span><span class="sxs-lookup"><span data-stu-id="077d5-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="077d5-105">Obtém a cor do plano de fundo da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="077d5-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="077d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="077d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="077d5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="077d5-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="077d5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="077d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="077d5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="077d5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="077d5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="077d5-111">Return value</span></span>

<span data-ttu-id="077d5-112">Retorna a cor do plano de fundo da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="077d5-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="077d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="077d5-113">Remarks</span></span>

<span data-ttu-id="077d5-114">Essa é a cor definida pela mensagem [**\_ SETBKCOLOR do PBM**](pbm-setbkcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="077d5-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="077d5-115">O valor padrão é CLR \_ padrão, que é definido em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="077d5-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="077d5-116">Essa função afeta apenas o modo clássico, não qualquer estilo visual.</span><span class="sxs-lookup"><span data-stu-id="077d5-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="077d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="077d5-117">Requirements</span></span>



| <span data-ttu-id="077d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="077d5-118">Requirement</span></span> | <span data-ttu-id="077d5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="077d5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="077d5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="077d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="077d5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="077d5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="077d5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="077d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="077d5-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="077d5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="077d5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="077d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="077d5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="077d5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





