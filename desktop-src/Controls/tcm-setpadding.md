---
title: Mensagem de TCM_SETPADDING (commctrl. h)
description: Define a quantidade de espaço (preenchimento) em volta do ícone e do rótulo de cada guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setpadding TabCtrl.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Controles de TCM_SETPADDING de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754370"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="6fc15-105">\_Mensagem de AUTOpreenchimento do TCM</span><span class="sxs-lookup"><span data-stu-id="6fc15-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="6fc15-106">Define a quantidade de espaço (preenchimento) em volta do ícone e do rótulo de cada guia em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="6fc15-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="6fc15-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setpadding TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .</span><span class="sxs-lookup"><span data-stu-id="6fc15-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fc15-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fc15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fc15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc15-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um valor **int** que especifica a quantidade de preenchimento horizontal, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6fc15-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="6fc15-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um valor **int** que especifica a quantidade de preenchimento vertical, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6fc15-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc15-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fc15-112">Return value</span></span>

<span data-ttu-id="6fc15-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6fc15-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc15-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc15-114">Requirements</span></span>



| <span data-ttu-id="6fc15-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc15-115">Requirement</span></span> | <span data-ttu-id="6fc15-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc15-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc15-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc15-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc15-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fc15-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fc15-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc15-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc15-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fc15-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fc15-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fc15-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc15-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc15-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

