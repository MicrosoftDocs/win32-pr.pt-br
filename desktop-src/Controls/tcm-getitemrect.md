---
title: Mensagem de TCM_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador para uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Controles de TCM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824712"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="59dd4-105">\_Mensagem GETITEMRECT de TCM</span><span class="sxs-lookup"><span data-stu-id="59dd4-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="59dd4-106">Recupera o retângulo delimitador para uma guia em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="59dd4-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="59dd4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="59dd4-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="59dd4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59dd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59dd4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59dd4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59dd4-110">Índice da guia.</span><span class="sxs-lookup"><span data-stu-id="59dd4-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="59dd4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59dd4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59dd4-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador da guia, em coordenadas do visor.</span><span class="sxs-lookup"><span data-stu-id="59dd4-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59dd4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59dd4-113">Return value</span></span>

<span data-ttu-id="59dd4-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="59dd4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="59dd4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59dd4-115">Requirements</span></span>



| <span data-ttu-id="59dd4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59dd4-116">Requirement</span></span> | <span data-ttu-id="59dd4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="59dd4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59dd4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59dd4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59dd4-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59dd4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59dd4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59dd4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59dd4-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59dd4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59dd4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59dd4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59dd4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59dd4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

