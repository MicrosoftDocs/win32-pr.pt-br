---
title: Mensagem de ACM_ISPLAYING (commctrl. h)
description: Verifica se um clipe AVI (intercalado Audio-Video) está sendo reproduzido. Você pode enviar essa mensagem explicitamente ou usar a \_ macro de IsPlaying de animação.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Controles de ACM_ISPLAYING de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009077"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="75aa9-105">Mensagem de exibição do ACM \_</span><span class="sxs-lookup"><span data-stu-id="75aa9-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="75aa9-106">Verifica se um clipe AVI (intercalado Audio-Video) está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="75aa9-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="75aa9-107">Você pode enviar essa mensagem explicitamente ou usar a macro de [**\_ IsPlaying de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .</span><span class="sxs-lookup"><span data-stu-id="75aa9-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="75aa9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75aa9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75aa9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75aa9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75aa9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="75aa9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75aa9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75aa9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75aa9-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="75aa9-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75aa9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75aa9-113">Return value</span></span>

<span data-ttu-id="75aa9-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="75aa9-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="75aa9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75aa9-115">Requirements</span></span>



| <span data-ttu-id="75aa9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75aa9-116">Requirement</span></span> | <span data-ttu-id="75aa9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="75aa9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75aa9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75aa9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75aa9-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75aa9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75aa9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75aa9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75aa9-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75aa9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75aa9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75aa9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75aa9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75aa9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





