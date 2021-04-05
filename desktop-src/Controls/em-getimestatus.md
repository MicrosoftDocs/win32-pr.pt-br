---
title: Mensagem de EM_GETIMESTATUS (WinUser. h)
description: Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (editor de método de entrada).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Controles de EM_GETIMESTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086036"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="eb7f4-104">\_Mensagem em GETIMESTATUS</span><span class="sxs-lookup"><span data-stu-id="eb7f4-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="eb7f4-105">Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="eb7f4-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="eb7f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb7f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb7f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7f4-108">O tipo de status a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-108">The type of status to retrieve.</span></span> <span data-ttu-id="eb7f4-109">Esse parâmetro pode ser o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="eb7f4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="eb7f4-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="eb7f4-111">Significado</span><span class="sxs-lookup"><span data-stu-id="eb7f4-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="eb7f4-112"><dt>**\_COMposicionastring EMSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7f4-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="eb7f4-113">Define o comportamento para manipular a cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eb7f4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb7f4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb7f4-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7f4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb7f4-116">Return value</span></span>

<span data-ttu-id="eb7f4-117">Dados específicos do tipo de status a recuperar.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="eb7f4-118">Com o valor **EMSIS \_ CompositionString** para *status*, esse valor de retorno é um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="eb7f4-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eb7f4-119">Return code</span></span>                                                                                                    | <span data-ttu-id="eb7f4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb7f4-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb7f4-121"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7f4-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="eb7f4-122">Se esse sinalizador for definido, o controle de edição acoplará a mensagem de [**\_ \_ composição IME do WM**](/windows/desktop/Intl/wm-ime-composition) com *fFlags* definido como GCS \_ RESULTSTR e retornará a cadeia de caracteres de resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="eb7f4-123">Se esse sinalizador não for definido, o controle de edição passará a mensagem de **\_ \_ composição IME do WM** para o procedimento de janela padrão e processará a cadeia de caracteres de resultado da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ; esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="eb7f4-124"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7f4-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="eb7f4-125">Se esse sinalizador for definido, o controle de edição cancelará a cadeia de caracteres de composição quando receber a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="eb7f4-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="eb7f4-126">Se esse sinalizador não for definido, o controle de edição não cancelará a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="eb7f4-127"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="eb7f4-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="eb7f4-128">Se esse sinalizador for definido, o controle de edição concluirá a cadeia de caracteres de composição após receber a mensagem [**\_ KILLFOCUS do WM**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="eb7f4-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="eb7f4-129">Se esse sinalizador não for definido, o controle de edição não concluirá a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="eb7f4-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb7f4-130">Remarks</span></span>

<span data-ttu-id="eb7f4-131">**Edição avançada:** Não há suporte para a mensagem em **\_ GETIMESTATUS** .</span><span class="sxs-lookup"><span data-stu-id="eb7f4-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb7f4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb7f4-132">Requirements</span></span>



| <span data-ttu-id="eb7f4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7f4-133">Requirement</span></span> | <span data-ttu-id="eb7f4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="eb7f4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7f4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb7f4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="eb7f4-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb7f4-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb7f4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb7f4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="eb7f4-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb7f4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb7f4-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb7f4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb7f4-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb7f4-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7f4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb7f4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7f4-142">**em \_ SETIMESTATUS**</span><span class="sxs-lookup"><span data-stu-id="eb7f4-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

