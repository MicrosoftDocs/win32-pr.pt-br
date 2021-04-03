---
title: Mensagem de SBM_ENABLE_ARROWS (WinUser. h)
description: Um aplicativo envia a mensagem de SBM \_ habilitar \_ setas para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Controles de SBM_ENABLE_ARROWS de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918864"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="2e191-104">Mensagem de SBM \_ habilitar \_ setas</span><span class="sxs-lookup"><span data-stu-id="2e191-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="2e191-105">Um aplicativo envia a mensagem de **SBM \_ habilitar \_ setas** para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2e191-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e191-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e191-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e191-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e191-108">Especifica se as setas da barra de rolagem estão habilitadas ou desabilitadas e indica quais setas estão habilitadas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="2e191-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="2e191-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e191-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2e191-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2e191-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="2e191-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2e191-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="2e191-112"><dt>**ESB \_ desabilita \_ ambos**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="2e191-113">Desabilita ambas as setas em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2e191-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="2e191-114"><dt>**\_desabilitação do ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="2e191-115">Desabilita a seta para baixo em uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="2e191-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="2e191-116"><dt>**\_LTUP de desabilitação de ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="2e191-117">Desabilita a seta para a esquerda em uma barra de rolagem horizontal ou na seta para cima em uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="2e191-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="2e191-118"><dt>**\_desabilitação do ESB \_ restante**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="2e191-119">Desabilita a seta para a esquerda em uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="2e191-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="2e191-120"><dt>**\_RTDN de desabilitação de ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="2e191-121">Desabilita a seta para a direita em uma barra de rolagem horizontal ou na seta para baixo em uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="2e191-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="2e191-122"><dt>**\_desabilitação do ESB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="2e191-123">Desabilita a seta para cima em uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="2e191-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="2e191-124"><dt>**habilitado para ESB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="2e191-125">Habilita ambas as setas em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="2e191-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="2e191-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e191-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e191-127">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="2e191-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e191-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e191-128">Return value</span></span>

<span data-ttu-id="2e191-129">Se a mensagem tiver sucesso, o valor de retorno será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="2e191-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e191-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e191-130">Requirements</span></span>



| <span data-ttu-id="2e191-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e191-131">Requirement</span></span> | <span data-ttu-id="2e191-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2e191-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e191-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e191-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2e191-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e191-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e191-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e191-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2e191-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e191-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e191-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e191-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e191-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e191-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





