---
title: Mensagem de CB_GETDROPPEDCONTROLRECT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de GETDROPPEDCONTROLRECT CB para recuperar as coordenadas de tela de uma caixa de combinação em seu estado suspenso.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Controles de CB_GETDROPPEDCONTROLRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455352"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="fb4b6-104">\_Mensagem de GETDROPPEDCONTROLRECT CB</span><span class="sxs-lookup"><span data-stu-id="fb4b6-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="fb4b6-105">Um aplicativo envia uma mensagem de **\_ GETDROPPEDCONTROLRECT CB** para recuperar as coordenadas de tela de uma caixa de combinação em seu estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb4b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb4b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb4b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb4b6-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fb4b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb4b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb4b6-110">Um ponteiro para a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe as coordenadas da caixa de combinação em seu estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4b6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb4b6-111">Return value</span></span>

<span data-ttu-id="fb4b6-112">Se a mensagem tiver sucesso, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="fb4b6-113">Se a mensagem falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4b6-114">Requirements</span></span>



| <span data-ttu-id="fb4b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4b6-115">Requirement</span></span> | <span data-ttu-id="fb4b6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fb4b6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4b6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4b6-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb4b6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb4b6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4b6-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb4b6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb4b6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb4b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4b6-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb4b6-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4b6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb4b6-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb4b6-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb4b6-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

