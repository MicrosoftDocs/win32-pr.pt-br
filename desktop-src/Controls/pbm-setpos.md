---
title: Mensagem de PBM_SETPOS (commctrl. h)
description: Define a posição atual de uma barra de progresso e redesenha a barra para refletir a nova posição.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Controles de PBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755654"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="c4a6c-104">Mensagem do SETPOS do PBM \_</span><span class="sxs-lookup"><span data-stu-id="c4a6c-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="c4a6c-105">Define a posição atual de uma barra de progresso e redesenha a barra para refletir a nova posição.</span><span class="sxs-lookup"><span data-stu-id="c4a6c-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4a6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4a6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a6c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4a6c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a6c-108">Inteiro assinado que se torna a nova posição.</span><span class="sxs-lookup"><span data-stu-id="c4a6c-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="c4a6c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4a6c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c4a6c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c4a6c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a6c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4a6c-111">Return value</span></span>

<span data-ttu-id="c4a6c-112">Retorna a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="c4a6c-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a6c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4a6c-113">Remarks</span></span>

<span data-ttu-id="c4a6c-114">Se *wParam* estiver fora do intervalo do controle, a posição será definida como o limite mais próximo.</span><span class="sxs-lookup"><span data-stu-id="c4a6c-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="c4a6c-115">Não envie essa mensagem para um controle que tenha o estilo [**de \_ letreiro do PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a6c-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a6c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a6c-116">Requirements</span></span>



| <span data-ttu-id="c4a6c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a6c-117">Requirement</span></span> | <span data-ttu-id="c4a6c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a6c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a6c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a6c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a6c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4a6c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4a6c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a6c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a6c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4a6c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4a6c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4a6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a6c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a6c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





