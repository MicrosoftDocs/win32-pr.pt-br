---
title: Mensagem de RB_GETBANDBORDERS (commctrl. h)
description: Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área utilizável em uma banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Controles de RB_GETBANDBORDERS de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918781"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="4b6dc-105">\_Mensagem GETBANDBORDERS RB</span><span class="sxs-lookup"><span data-stu-id="4b6dc-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="4b6dc-106">Recupera as bordas de uma banda.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="4b6dc-107">O resultado dessa mensagem pode ser usado para calcular a área utilizável em uma banda.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b6dc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b6dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b6dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b6dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6dc-110">Índice de base zero da banda para a qual as bordas serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="4b6dc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b6dc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6dc-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as bordas da faixa.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="4b6dc-113">Se o controle rebar tiver o estilo [**RBS \_ BANDBORDERS**](rebar-control-styles.md) , cada membro dessa estrutura receberá o número de pixels, no lado correspondente da faixa, que constitui a borda.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="4b6dc-114">Se o controle rebar não tiver o estilo **RBS \_ BANDBORDERS** , somente o membro **à esquerda** dessa estrutura receberá informações válidas.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b6dc-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b6dc-115">Return value</span></span>

<span data-ttu-id="4b6dc-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6dc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b6dc-117">Requirements</span></span>



| <span data-ttu-id="4b6dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b6dc-118">Requirement</span></span> | <span data-ttu-id="4b6dc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4b6dc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6dc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b6dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b6dc-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b6dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b6dc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b6dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b6dc-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b6dc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b6dc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b6dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b6dc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b6dc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

