---
title: Mensagem de EM_SETIMESTATUS (WinUser. h)
description: Define os sinalizadores de status que determinam como um controle de edição interage com o IME (editor de método de entrada).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Controles de EM_SETIMESTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644777"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="cbdc1-104">\_Mensagem em SETIMESTATUS</span><span class="sxs-lookup"><span data-stu-id="cbdc1-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="cbdc1-105">Define os sinalizadores de status que determinam como um controle de edição interage com o IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="cbdc1-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="cbdc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbdc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbdc1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbdc1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbdc1-108">O tipo de status a ser definido.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-108">The type of status to set.</span></span> <span data-ttu-id="cbdc1-109">Esse parâmetro pode ser o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="cbdc1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="cbdc1-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="cbdc1-111">Significado</span><span class="sxs-lookup"><span data-stu-id="cbdc1-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="cbdc1-112"><dt>**\_COMposicionastring EMSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc1-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="cbdc1-113">Define o comportamento para a cadeia de caracteres de composição de manipulação.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cbdc1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbdc1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbdc1-115">Dados específicos para o tipo de status.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-115">Data specific to the status type.</span></span> <span data-ttu-id="cbdc1-116">Se *wParam* for **EMSIS \_ CompositionString**, esse parâmetro poderá ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cbdc1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cbdc1-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="cbdc1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cbdc1-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="cbdc1-119"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc1-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="cbdc1-120">Se esse sinalizador for definido, o controle de edição acoplará a mensagem de [**\_ \_ composição do IME do WM**](/windows/desktop/Intl/wm-ime-composition) com *lParam* definido como GCS \_ RESULTSTR e retornará a cadeia de caracteres de resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="cbdc1-121">Se esse sinalizador não for definido, o controle de edição passará a mensagem de **\_ \_ composição IME do WM** para o procedimento de janela padrão e manipulará a cadeia de caracteres de resultado da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ; esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="cbdc1-122"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc1-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="cbdc1-123">Se esse sinalizador for definido, o controle de edição cancelará a cadeia de caracteres de composição quando receber a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="cbdc1-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="cbdc1-124">Se esse sinalizador não for definido, o controle de edição não cancelará a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="cbdc1-125"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc1-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="cbdc1-126">Se esse sinalizador for definido, o controle de edição concluirá a cadeia de caracteres de composição após receber a mensagem [**\_ KILLFOCUS do WM**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="cbdc1-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="cbdc1-127">Se esse sinalizador não for definido, o controle de edição não concluirá a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbdc1-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbdc1-128">Return value</span></span>

<span data-ttu-id="cbdc1-129">Retorna o valor anterior do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cbdc1-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbdc1-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbdc1-130">Remarks</span></span>

<span data-ttu-id="cbdc1-131">**Edição avançada:** Não há suporte para a mensagem em **\_ SETIMESTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cbdc1-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbdc1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbdc1-132">Requirements</span></span>



| <span data-ttu-id="cbdc1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbdc1-133">Requirement</span></span> | <span data-ttu-id="cbdc1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cbdc1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdc1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbdc1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdc1-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbdc1-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbdc1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbdc1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdc1-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbdc1-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cbdc1-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbdc1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbdc1-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc1-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdc1-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbdc1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdc1-142">**em \_ GETIMESTATUS**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

