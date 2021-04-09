---
description: Enviado a um aplicativo quando o IME altera o status da composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Mensagem de WM_IME_COMPOSITION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922905"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="6463b-104">Mensagem de composição do \_ IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="6463b-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="6463b-105">Enviado a um aplicativo quando o IME altera o status da composição como resultado de um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="6463b-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="6463b-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6463b-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="6463b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6463b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6463b-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6463b-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6463b-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="6463b-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6463b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6463b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6463b-111">Caractere DBCS que representa a alteração mais recente na cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="6463b-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="6463b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6463b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6463b-113">Valor que especifica como a cadeia de caracteres de composição ou o caractere foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6463b-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="6463b-114">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6463b-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="6463b-115">Para obter mais informações sobre esses valores, consulte [valores da cadeia de caracteres de composição do IME](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="6463b-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="6463b-116">**GCS \_ COMPATTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="6463b-117">**GCS \_ COMPCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="6463b-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="6463b-118">**GCS \_ COMPREADSTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="6463b-119">**GCS \_ COMPREADATTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="6463b-120">**GCS \_ COMPREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="6463b-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="6463b-121">**GCS \_ COMPSTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="6463b-122">**GCS \_ CURSORPOS**</span><span class="sxs-lookup"><span data-stu-id="6463b-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="6463b-123">**GCS \_ DELTASTART**</span><span class="sxs-lookup"><span data-stu-id="6463b-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="6463b-124">**GCS \_ RESULTCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="6463b-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="6463b-125">**GCS \_ RESULTREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="6463b-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="6463b-126">**GCS \_ RESULTREADSTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="6463b-127">**GCS \_ RESULTSTR**</span><span class="sxs-lookup"><span data-stu-id="6463b-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="6463b-128">O parâmetro *lParam* também pode ter um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6463b-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="6463b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6463b-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="6463b-130">Significado</span><span class="sxs-lookup"><span data-stu-id="6463b-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="6463b-131"><dt>**CS \_ INSERTCHAR**</dt></span><span class="sxs-lookup"><span data-stu-id="6463b-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="6463b-132">Inserir o caractere de composição *wParam* no ponto de inserção atual.</span><span class="sxs-lookup"><span data-stu-id="6463b-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="6463b-133">Um aplicativo deverá exibir o caractere de composição se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6463b-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="6463b-134"><dt>**CS \_ NOMOVECARET**</dt></span><span class="sxs-lookup"><span data-stu-id="6463b-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="6463b-135">Não mova a posição do cursor como resultado do processamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6463b-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="6463b-136">Por exemplo, se um IME especificar uma combinação de CS \_ INSERTCHAR e cs \_ NOMOVECARET, o aplicativo deverá inserir o caractere especificado na posição atual do cursor, mas não deverá mover o cursor para a próxima posição.</span><span class="sxs-lookup"><span data-stu-id="6463b-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="6463b-137">Uma mensagem de composição do IME do WM subsequente \_ \_ com GCS \_ RESULTSTR substituirá esse caractere.</span><span class="sxs-lookup"><span data-stu-id="6463b-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6463b-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6463b-138">Return value</span></span>

<span data-ttu-id="6463b-139">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6463b-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6463b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="6463b-140">Remarks</span></span>

<span data-ttu-id="6463b-141">Um aplicativo deve processar essa mensagem se exibir os próprios caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="6463b-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="6463b-142">Caso contrário, ele deve enviar a mensagem para a janela do IME.</span><span class="sxs-lookup"><span data-stu-id="6463b-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="6463b-143">Se o aplicativo tiver criado uma janela IME, ele deverá passar essa mensagem para essa janela.</span><span class="sxs-lookup"><span data-stu-id="6463b-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="6463b-144">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando-a para a janela padrão do IME.</span><span class="sxs-lookup"><span data-stu-id="6463b-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="6463b-145">A janela IME processa essa mensagem atualizando sua aparência com base no sinalizador de alteração especificado.</span><span class="sxs-lookup"><span data-stu-id="6463b-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="6463b-146">Um aplicativo pode chamar [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) para recuperar o novo status de composição.</span><span class="sxs-lookup"><span data-stu-id="6463b-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="6463b-147">Se nenhum dos valores de GCS \_ for definido, a mensagem indicará que a composição atual foi cancelada e os aplicativos que desenharem a cadeia de caracteres de composição devem excluir a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6463b-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="6463b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6463b-148">Requirements</span></span>



| <span data-ttu-id="6463b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6463b-149">Requirement</span></span> | <span data-ttu-id="6463b-150">Valor</span><span class="sxs-lookup"><span data-stu-id="6463b-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6463b-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6463b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6463b-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6463b-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="6463b-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6463b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6463b-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6463b-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6463b-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6463b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6463b-156"><dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6463b-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6463b-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="6463b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6463b-158">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="6463b-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6463b-159">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="6463b-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="6463b-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="6463b-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
