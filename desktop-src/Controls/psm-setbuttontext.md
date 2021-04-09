---
title: Mensagem de PSM_SETBUTTONTEXT (Prsht. h)
description: Define o texto em um botão em um assistente de Aero. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Controles de PSM_SETBUTTONTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009260"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="948c2-105">Mensagem de PSM \_ SETBUTTONTEXT</span><span class="sxs-lookup"><span data-stu-id="948c2-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="948c2-106">Define o texto em um botão em um assistente de Aero.</span><span class="sxs-lookup"><span data-stu-id="948c2-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="948c2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .</span><span class="sxs-lookup"><span data-stu-id="948c2-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="948c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="948c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="948c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="948c2-110">Um dos valores a seguir especificando o botão cujo texto está definido.</span><span class="sxs-lookup"><span data-stu-id="948c2-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="948c2-111">Valor</span><span class="sxs-lookup"><span data-stu-id="948c2-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="948c2-112">Significado</span><span class="sxs-lookup"><span data-stu-id="948c2-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="948c2-113"><dt>**PSWIZB \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="948c2-114">O botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="948c2-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="948c2-115"><dt>**PSWIZB \_ cancelar**</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="948c2-116">O botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="948c2-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="948c2-117"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="948c2-118">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="948c2-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="948c2-119"><dt>**PSWIZB \_ concluir**</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="948c2-120">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="948c2-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="948c2-121"><dt>**PSWIZB \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="948c2-122">O botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="948c2-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="948c2-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="948c2-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="948c2-124">O texto a ser definido.</span><span class="sxs-lookup"><span data-stu-id="948c2-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948c2-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="948c2-125">Return value</span></span>

<span data-ttu-id="948c2-126">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="948c2-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="948c2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948c2-127">Requirements</span></span>



| <span data-ttu-id="948c2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="948c2-128">Requirement</span></span> | <span data-ttu-id="948c2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="948c2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="948c2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="948c2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="948c2-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="948c2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="948c2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="948c2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="948c2-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="948c2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="948c2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="948c2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="948c2-135"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="948c2-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="948c2-136">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="948c2-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="948c2-137">**PSM \_ SETBUTTONTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="948c2-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





