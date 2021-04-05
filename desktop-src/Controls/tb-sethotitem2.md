---
title: Mensagem de TB_SETHOTITEM2 (commctrl. h)
description: Define o item ativo em uma barra de ferramentas.
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
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644937"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="11bae-104">TB de \_ mensagem SETHOTITEM2</span><span class="sxs-lookup"><span data-stu-id="11bae-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="11bae-105">Define o item ativo em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="11bae-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="11bae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11bae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11bae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11bae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11bae-108">Índice do item que se tornará quente.</span><span class="sxs-lookup"><span data-stu-id="11bae-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="11bae-109">Se esse valor for-1, nenhum dos itens será quente.</span><span class="sxs-lookup"><span data-stu-id="11bae-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="11bae-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11bae-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="11bae-111">Uma combinação de \_ sinalizadores HICF xxx.</span><span class="sxs-lookup"><span data-stu-id="11bae-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="11bae-112">Consulte <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="11bae-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11bae-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11bae-113">Return value</span></span>

<span data-ttu-id="11bae-114">Retorna o índice do item ativo anterior, ou-1 se não houver nenhum item ativo.</span><span class="sxs-lookup"><span data-stu-id="11bae-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="11bae-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="11bae-115">Remarks</span></span>

<span data-ttu-id="11bae-116">O comportamento dessa mensagem não é definido para barras de ferramentas que não têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="11bae-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bae-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11bae-117">Requirements</span></span>



| <span data-ttu-id="11bae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11bae-118">Requirement</span></span> | <span data-ttu-id="11bae-119">Valor</span><span class="sxs-lookup"><span data-stu-id="11bae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11bae-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11bae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11bae-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11bae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11bae-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11bae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11bae-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11bae-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11bae-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11bae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11bae-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="11bae-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





