---
title: Mensagem de PBM_GETSTEP (commctrl. h)
description: Recupera a etapa incremento de uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma \_ mensagem STEPIT do PBM. Por padrão, o incremento Step é definido como 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Controles de PBM_GETSTEP de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918793"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="59fc5-106">Mensagem do PBM \_ GETstep</span><span class="sxs-lookup"><span data-stu-id="59fc5-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="59fc5-107">Recupera a etapa incremento de uma barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="59fc5-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="59fc5-108">A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="59fc5-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="59fc5-109">Por padrão, o incremento Step é definido como 10.</span><span class="sxs-lookup"><span data-stu-id="59fc5-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="59fc5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59fc5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fc5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59fc5-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59fc5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="59fc5-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59fc5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59fc5-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59fc5-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="59fc5-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fc5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59fc5-115">Return value</span></span>

<span data-ttu-id="59fc5-116">Retorna o incremento da etapa atual.</span><span class="sxs-lookup"><span data-stu-id="59fc5-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="59fc5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59fc5-117">Requirements</span></span>



| <span data-ttu-id="59fc5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59fc5-118">Requirement</span></span> | <span data-ttu-id="59fc5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="59fc5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59fc5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59fc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59fc5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59fc5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59fc5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59fc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59fc5-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59fc5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59fc5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59fc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59fc5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59fc5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





