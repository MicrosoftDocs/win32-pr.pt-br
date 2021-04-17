---
title: Mensagem de ACM_PLAY (commctrl. h)
description: Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ reprodução de animação.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Controles de ACM_PLAY de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454827"
---
# <a name="acm_play-message"></a><span data-ttu-id="febe8-106">Mensagem de reprodução do ACM \_</span><span class="sxs-lookup"><span data-stu-id="febe8-106">ACM\_PLAY message</span></span>

<span data-ttu-id="febe8-107">Reproduz um clipe AVI em um controle de animação.</span><span class="sxs-lookup"><span data-stu-id="febe8-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="febe8-108">O controle reproduz o clipe em segundo plano enquanto o thread continua em execução.</span><span class="sxs-lookup"><span data-stu-id="febe8-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="febe8-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ reprodução de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .</span><span class="sxs-lookup"><span data-stu-id="febe8-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="febe8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="febe8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febe8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="febe8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="febe8-112">Um **uint** que especifica o número de vezes para reproduzir o clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="febe8-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="febe8-113">Um valor de-1 significa repetir o clipe indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="febe8-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="febe8-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="febe8-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="febe8-115">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o índice de base zero do quadro em que a execução é iniciada.</span><span class="sxs-lookup"><span data-stu-id="febe8-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="febe8-116">O valor deve ser menor que 65.536.</span><span class="sxs-lookup"><span data-stu-id="febe8-116">The value must be less than 65,536.</span></span> <span data-ttu-id="febe8-117">Um valor de zero significa começar com o primeiro quadro no clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="febe8-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="febe8-118">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é o índice de base zero do quadro em que a execução termina.</span><span class="sxs-lookup"><span data-stu-id="febe8-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="febe8-119">O valor deve ser menor que 65.536.</span><span class="sxs-lookup"><span data-stu-id="febe8-119">The value must be less than 65,536.</span></span> <span data-ttu-id="febe8-120">Um valor de-1 significa terminar com o último quadro no clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="febe8-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febe8-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="febe8-121">Return value</span></span>

<span data-ttu-id="febe8-122">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="febe8-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="febe8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="febe8-123">Remarks</span></span>

<span data-ttu-id="febe8-124">Você pode usar o [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) para direcionar o controle de animação para exibir um quadro específico do clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="febe8-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="febe8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="febe8-125">Requirements</span></span>



| <span data-ttu-id="febe8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="febe8-126">Requirement</span></span> | <span data-ttu-id="febe8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="febe8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="febe8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="febe8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="febe8-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="febe8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="febe8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="febe8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="febe8-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="febe8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="febe8-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="febe8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="febe8-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="febe8-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

