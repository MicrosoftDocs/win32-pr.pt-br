---
title: Mensagem de ACM_STOP (commctrl. h)
description: Interrompe a reprodução de um clipe AVI em um controle de animação. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ parada de animação.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Controles de ACM_STOP de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085292"
---
# <a name="acm_stop-message"></a><span data-ttu-id="4ed5c-105">Mensagem de parada do ACM \_</span><span class="sxs-lookup"><span data-stu-id="4ed5c-105">ACM\_STOP message</span></span>

<span data-ttu-id="4ed5c-106">Interrompe a reprodução de um clipe AVI em um controle de animação.</span><span class="sxs-lookup"><span data-stu-id="4ed5c-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="4ed5c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ parada de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .</span><span class="sxs-lookup"><span data-stu-id="4ed5c-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ed5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ed5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed5c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ed5c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4ed5c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4ed5c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4ed5c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ed5c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4ed5c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4ed5c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed5c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ed5c-113">Return value</span></span>

<span data-ttu-id="4ed5c-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="4ed5c-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed5c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed5c-115">Requirements</span></span>



| <span data-ttu-id="4ed5c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed5c-116">Requirement</span></span> | <span data-ttu-id="4ed5c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4ed5c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed5c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed5c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed5c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ed5c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ed5c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed5c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed5c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ed5c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ed5c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ed5c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed5c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed5c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





