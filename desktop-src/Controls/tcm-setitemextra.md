---
title: Mensagem de TCM_SETITEMEXTRA (commctrl. h)
description: Define o número de bytes por tabulação reservados para dados definidos pelo aplicativo em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Controles de TCM_SETITEMEXTRA de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085151"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="9f373-105">\_Mensagem SETITEMEXTRA de TCM</span><span class="sxs-lookup"><span data-stu-id="9f373-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="9f373-106">Define o número de bytes por tabulação reservados para dados definidos pelo aplicativo em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="9f373-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="9f373-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .</span><span class="sxs-lookup"><span data-stu-id="9f373-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f373-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f373-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f373-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f373-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f373-110">Número de bytes extras.</span><span class="sxs-lookup"><span data-stu-id="9f373-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9f373-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f373-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f373-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9f373-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f373-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f373-113">Return value</span></span>

<span data-ttu-id="9f373-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9f373-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f373-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f373-115">Remarks</span></span>

<span data-ttu-id="9f373-116">Por padrão, o número de bytes extras é quatro.</span><span class="sxs-lookup"><span data-stu-id="9f373-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="9f373-117">Um aplicativo que altera o número de bytes extras não pode usar a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar e definir os dados definidos pelo aplicativo para uma guia. Em vez disso, você deve definir uma nova estrutura que consiste na estrutura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguida por membros definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f373-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="9f373-118">Um aplicativo só deve alterar o número de bytes extras quando um controle guia não contiver nenhuma tabulação.</span><span class="sxs-lookup"><span data-stu-id="9f373-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f373-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f373-119">Requirements</span></span>



| <span data-ttu-id="9f373-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f373-120">Requirement</span></span> | <span data-ttu-id="9f373-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9f373-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f373-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f373-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f373-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f373-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f373-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f373-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f373-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f373-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f373-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f373-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f373-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f373-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





