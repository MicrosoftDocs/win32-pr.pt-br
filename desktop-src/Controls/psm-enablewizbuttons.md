---
title: Mensagem de PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Habilita ou desabilita qualquer um dos botões padrão em um assistente Aero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Controles de PSM_ENABLEWIZBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918699"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="212eb-105">Mensagem de PSM \_ ENABLEWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="212eb-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="212eb-106">Habilita ou desabilita qualquer um dos botões padrão em um assistente Aero.</span><span class="sxs-lookup"><span data-stu-id="212eb-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="212eb-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="212eb-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="212eb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="212eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="212eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="212eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="212eb-110">Um ou mais dos valores a seguir que especificam quais botões de folha de propriedades devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="212eb-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="212eb-111">Se um valor de botão for incluído nesse parâmetro e no *lParam*, ele será habilitado.</span><span class="sxs-lookup"><span data-stu-id="212eb-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="212eb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="212eb-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="212eb-113">Significado</span><span class="sxs-lookup"><span data-stu-id="212eb-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="212eb-114"><dt>**PSWIZB \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="212eb-115">O botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="212eb-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="212eb-116"><dt>**PSWIZB \_ cancelar**</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="212eb-117">O botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="212eb-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="212eb-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="212eb-119">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="212eb-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="212eb-120"><dt>**PSWIZB \_ concluir**</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="212eb-121">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="212eb-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="212eb-122"><dt>**PSWIZB \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="212eb-123">O botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="212eb-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="212eb-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="212eb-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="212eb-125">Um ou mais dos mesmos valores usados em *wParam*, especificando quais botões são afetados por essa chamada.</span><span class="sxs-lookup"><span data-stu-id="212eb-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="212eb-126">Se um valor de botão aparecer nesse parâmetro, mas não em *wParam*, ele indicará que o botão deve ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="212eb-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="212eb-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="212eb-127">Return value</span></span>

<span data-ttu-id="212eb-128">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="212eb-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="212eb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="212eb-129">Requirements</span></span>



| <span data-ttu-id="212eb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="212eb-130">Requirement</span></span> | <span data-ttu-id="212eb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="212eb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="212eb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="212eb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="212eb-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="212eb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="212eb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="212eb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="212eb-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="212eb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="212eb-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="212eb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="212eb-137"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="212eb-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





