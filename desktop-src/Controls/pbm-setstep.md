---
title: Mensagem de PBM_SETSTEP (commctrl. h)
description: Especifica o incremento de etapa para uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma \_ mensagem STEPIT do PBM. Por padrão, o incremento Step é definido como 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Controles de PBM_SETSTEP de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754809"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="6c0dd-106">\_Mensagem de SETstep do PBM</span><span class="sxs-lookup"><span data-stu-id="6c0dd-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="6c0dd-107">Especifica o incremento de etapa para uma barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="6c0dd-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="6c0dd-108">A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0dd-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="6c0dd-109">Por padrão, o incremento Step é definido como 10.</span><span class="sxs-lookup"><span data-stu-id="6c0dd-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c0dd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c0dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0dd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c0dd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c0dd-112">Incremento de nova etapa.</span><span class="sxs-lookup"><span data-stu-id="6c0dd-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="6c0dd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c0dd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6c0dd-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6c0dd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0dd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c0dd-115">Return value</span></span>

<span data-ttu-id="6c0dd-116">Retorna o incremento da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="6c0dd-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c0dd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c0dd-117">Requirements</span></span>



| <span data-ttu-id="6c0dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c0dd-118">Requirement</span></span> | <span data-ttu-id="6c0dd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6c0dd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0dd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c0dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0dd-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c0dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c0dd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c0dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0dd-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c0dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c0dd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c0dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c0dd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c0dd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





