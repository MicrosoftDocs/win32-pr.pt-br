---
title: Mensagem de MCM_GETMAXSELCOUNT (commctrl. h)
description: Recupera o intervalo de datas máximo que pode ser selecionado em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Controles de MCM_GETMAXSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009522"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="a558c-105">\_Mensagem MCM GETMAXSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="a558c-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="a558c-106">Recupera o intervalo de datas máximo que pode ser selecionado em um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="a558c-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="a558c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="a558c-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a558c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a558c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a558c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a558c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a558c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a558c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a558c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a558c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a558c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a558c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a558c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a558c-113">Return value</span></span>

<span data-ttu-id="a558c-114">Retorna um valor INT que representa o número total de dias que podem ser selecionados para o controle.</span><span class="sxs-lookup"><span data-stu-id="a558c-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a558c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a558c-115">Remarks</span></span>

<span data-ttu-id="a558c-116">Você pode alterar o intervalo de datas máximo que pode ser selecionado usando a mensagem [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="a558c-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a558c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a558c-117">Requirements</span></span>



| <span data-ttu-id="a558c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a558c-118">Requirement</span></span> | <span data-ttu-id="a558c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a558c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a558c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a558c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a558c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a558c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a558c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a558c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a558c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a558c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a558c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a558c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a558c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a558c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





