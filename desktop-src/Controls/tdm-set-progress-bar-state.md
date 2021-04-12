---
title: Mensagem de TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Define o estado da barra de progresso em uma caixa de diálogo de tarefa.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Controles de TDM_SET_PROGRESS_BAR_STATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/08/2021
ms.locfileid: "104298056"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="6a6c1-104">\_Mensagem de \_ estado da barra de progresso do conjunto TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="6a6c1-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="6a6c1-105">Define o estado da barra de progresso em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a6c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a6c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a6c1-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6c1-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6c1-108">Um **int** que especifica o estado da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="6a6c1-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6a6c1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6a6c1-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="6a6c1-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6a6c1-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="6a6c1-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="6a6c1-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="6a6c1-113">Define a barra de progresso para o estado normal.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="6a6c1-114"><dt>**PBST em \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="6a6c1-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="6a6c1-115">Define a barra de progresso para o estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="6a6c1-116"><dt>**erro de PBST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a6c1-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="6a6c1-117">Defina a barra de progresso para o estado de erro.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="6a6c1-118">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6c1-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6c1-119">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a6c1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a6c1-120">Return value</span></span>

<span data-ttu-id="6a6c1-121">Se a função for realizada com sucesso, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="6a6c1-122">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="6a6c1-123">Para obter informações de erro estendidas, chame GetLastError.</span><span class="sxs-lookup"><span data-stu-id="6a6c1-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a6c1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a6c1-124">Requirements</span></span>



| <span data-ttu-id="6a6c1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a6c1-125">Requirement</span></span> | <span data-ttu-id="6a6c1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6a6c1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6c1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a6c1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a6c1-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a6c1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a6c1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a6c1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a6c1-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a6c1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a6c1-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a6c1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a6c1-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a6c1-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





