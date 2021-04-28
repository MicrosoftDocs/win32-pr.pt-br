---
title: Mensagem de TB_SETHOTITEM2 (commctrl. h)
description: TB_SETHOTITEM2 mensagem – define o item ativo em uma barra de ferramentas.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Controles de TB_SETHOTITEM2 de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104134"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="d8db0-104">TB de \_ mensagem SETHOTITEM2</span><span class="sxs-lookup"><span data-stu-id="d8db0-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="d8db0-105">Define o item ativo em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d8db0-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8db0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8db0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8db0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8db0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8db0-108">Índice do item que se tornará quente.</span><span class="sxs-lookup"><span data-stu-id="d8db0-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="d8db0-109">Se esse valor for-1, nenhum dos itens será quente.</span><span class="sxs-lookup"><span data-stu-id="d8db0-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="d8db0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8db0-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d8db0-111">Uma combinação de \_ sinalizadores HICF xxx.</span><span class="sxs-lookup"><span data-stu-id="d8db0-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="d8db0-112">Consulte <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="d8db0-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8db0-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d8db0-113">Return value</span></span>

<span data-ttu-id="d8db0-114">Retorna o índice do item ativo anterior, ou-1 se não houver nenhum item ativo.</span><span class="sxs-lookup"><span data-stu-id="d8db0-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8db0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8db0-115">Remarks</span></span>

<span data-ttu-id="d8db0-116">O comportamento dessa mensagem não é definido para barras de ferramentas que não têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d8db0-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8db0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8db0-117">Requirements</span></span>



| <span data-ttu-id="d8db0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8db0-118">Requirement</span></span> | <span data-ttu-id="d8db0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d8db0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8db0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8db0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8db0-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8db0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8db0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8db0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8db0-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8db0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8db0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8db0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8db0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8db0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





