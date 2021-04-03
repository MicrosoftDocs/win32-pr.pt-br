---
title: Mensagem de PBM_SETMARQUEE (commctrl. h)
description: Define a barra de progresso para o modo de letreiro. Isso faz com que a barra de progresso se mova como um letreiro.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Controles de PBM_SETMARQUEE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918792"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="ea44e-105">\_Mensagem SETmarquee do PBM</span><span class="sxs-lookup"><span data-stu-id="ea44e-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="ea44e-106">Define a barra de progresso para o modo de letreiro.</span><span class="sxs-lookup"><span data-stu-id="ea44e-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="ea44e-107">Isso faz com que a barra de progresso se mova como um letreiro.</span><span class="sxs-lookup"><span data-stu-id="ea44e-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea44e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea44e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea44e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea44e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea44e-110">Indica se o modo de letreiro deve ser ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="ea44e-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="ea44e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea44e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ea44e-112">Tempo, em milissegundos, entre as atualizações de animação do letreiro digital.</span><span class="sxs-lookup"><span data-stu-id="ea44e-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="ea44e-113">Se esse parâmetro for zero, a animação do letreiro digital será atualizada a cada 30 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ea44e-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea44e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea44e-114">Return value</span></span>

<span data-ttu-id="ea44e-115">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="ea44e-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea44e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea44e-116">Remarks</span></span>

<span data-ttu-id="ea44e-117">Use esta mensagem quando você não souber a quantidade de progresso para a conclusão, mas quiser indicar que o progresso está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="ea44e-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="ea44e-118">Envie a **mensagem \_ setmarquee do PBM** para iniciar ou parar a animação.</span><span class="sxs-lookup"><span data-stu-id="ea44e-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="ea44e-119">Você deve definir o estilo de controle [**como \_ marca de marcação PBS**](progress-bar-control-styles.md) antes de tentar iniciar a animação.</span><span class="sxs-lookup"><span data-stu-id="ea44e-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea44e-120">Esta mensagem requer ComCtl32.dll versão 6, 0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ea44e-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea44e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea44e-121">Requirements</span></span>



| <span data-ttu-id="ea44e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea44e-122">Requirement</span></span> | <span data-ttu-id="ea44e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea44e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea44e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea44e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea44e-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea44e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea44e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea44e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea44e-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea44e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea44e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea44e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea44e-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea44e-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





