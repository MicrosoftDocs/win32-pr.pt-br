---
title: Mensagem de PBM_STEPIT (commctrl. h)
description: Avança a posição atual de uma barra de progresso pela etapa incremento e redesenha a barra para refletir a nova posição. Um aplicativo define o incremento de etapa enviando a \_ mensagem do PBM SetStep.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Controles de PBM_STEPIT de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918789"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="62356-105">Mensagem do STEPIT do PBM \_</span><span class="sxs-lookup"><span data-stu-id="62356-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="62356-106">Avança a posição atual de uma barra de progresso pela etapa incremento e redesenha a barra para refletir a nova posição.</span><span class="sxs-lookup"><span data-stu-id="62356-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="62356-107">Um aplicativo define o incremento de etapa enviando a mensagem do [**PBM \_ SetStep**](pbm-setstep.md) .</span><span class="sxs-lookup"><span data-stu-id="62356-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="62356-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62356-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62356-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62356-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62356-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62356-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62356-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="62356-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62356-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62356-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62356-113">Return value</span></span>

<span data-ttu-id="62356-114">Retorna a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="62356-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="62356-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="62356-115">Remarks</span></span>

<span data-ttu-id="62356-116">Quando a posição excede o valor de intervalo máximo, essa mensagem redefine a posição atual para que o indicador de progresso comece novamente desde o início.</span><span class="sxs-lookup"><span data-stu-id="62356-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="62356-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62356-117">Requirements</span></span>



| <span data-ttu-id="62356-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62356-118">Requirement</span></span> | <span data-ttu-id="62356-119">Valor</span><span class="sxs-lookup"><span data-stu-id="62356-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62356-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62356-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62356-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62356-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62356-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62356-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62356-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62356-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62356-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62356-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62356-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62356-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





