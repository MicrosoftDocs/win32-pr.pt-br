---
title: Mensagem de PSM_PRESSBUTTON (Prsht. h)
description: Simula a seleção de um botão de folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Controles de PSM_PRESSBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456044"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="df6de-105">Mensagem de PSM \_ PRESSBUTTON</span><span class="sxs-lookup"><span data-stu-id="df6de-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="df6de-106">Simula a seleção de um botão de folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="df6de-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="df6de-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .</span><span class="sxs-lookup"><span data-stu-id="df6de-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df6de-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df6de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df6de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df6de-110">Índice do botão a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="df6de-110">Index of the button to select.</span></span> <span data-ttu-id="df6de-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="df6de-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="df6de-112">Valor</span><span class="sxs-lookup"><span data-stu-id="df6de-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="df6de-113">Significado</span><span class="sxs-lookup"><span data-stu-id="df6de-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="df6de-114"><dt>**PSBTN \_ APPLYNOW**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="df6de-115">Seleciona o botão **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="df6de-115">Selects the **Apply** button.</span></span> <span data-ttu-id="df6de-116">Esse valor não é válido ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="df6de-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="df6de-117"><dt>**PSBTN \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="df6de-118">Seleciona o botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="df6de-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="df6de-119"><dt>**PSBTN \_ cancelar**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="df6de-120">Seleciona o botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="df6de-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="df6de-121"><dt>**PSBTN \_ concluir**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="df6de-122">Seleciona o botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="df6de-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="df6de-123"><dt>**ajuda do PSBTN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="df6de-124">Seleciona o botão **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="df6de-124">Selects the **Help** button.</span></span> <span data-ttu-id="df6de-125">Esse valor não é válido ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="df6de-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="df6de-126"><dt>**PSBTN \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="df6de-127">Seleciona o botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="df6de-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="df6de-128"><dt>**PSBTN \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="df6de-129">Seleciona o botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="df6de-129">Selects the **OK** button.</span></span> <span data-ttu-id="df6de-130">Esse valor não é válido ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="df6de-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="df6de-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df6de-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df6de-132">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="df6de-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6de-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df6de-133">Return value</span></span>

<span data-ttu-id="df6de-134">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="df6de-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6de-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df6de-135">Requirements</span></span>



| <span data-ttu-id="df6de-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6de-136">Requirement</span></span> | <span data-ttu-id="df6de-137">Valor</span><span class="sxs-lookup"><span data-stu-id="df6de-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df6de-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df6de-138">Minimum supported client</span></span><br/> | <span data-ttu-id="df6de-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df6de-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df6de-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df6de-140">Minimum supported server</span></span><br/> | <span data-ttu-id="df6de-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df6de-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df6de-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df6de-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="df6de-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





