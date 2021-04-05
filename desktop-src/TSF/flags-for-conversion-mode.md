---
title: Sinalizadores para o modo de conversão (Ctffunc. h)
description: Os sinalizadores a seguir são usados como um valor da conversão de teclado do compartimento de GUID de \_ \_ \_ entrada \_ . Isso é equivalente a \_ valores de CMODE do IME para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Sinalizadores para a estrutura de serviços de texto do modo de conversão
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085703"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="0ed62-105">Sinalizadores para o modo de conversão</span><span class="sxs-lookup"><span data-stu-id="0ed62-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="0ed62-106">Os sinalizadores a seguir são usados como um valor da [conversão de teclado do compartimento de GUID de \_ \_ \_ entrada \_ ](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="0ed62-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="0ed62-107">Isso é equivalente a valores de [ \_ CMODE do IME](../intl/ime-conversion-mode-values.md) para IMM32.</span><span class="sxs-lookup"><span data-stu-id="0ed62-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="0ed62-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="0ed62-108">Flag</span></span>                             | <span data-ttu-id="0ed62-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0ed62-109">Value</span></span>  | <span data-ttu-id="0ed62-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ed62-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="0ed62-111">TF \_ CONversãomode \_ alfanumérico</span><span class="sxs-lookup"><span data-stu-id="0ed62-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="0ed62-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="0ed62-112">0x0000</span></span> | <span data-ttu-id="0ed62-113">Defina como 1 se o modo alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="0ed62-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="0ed62-114">TF \_ CONversãomode \_ nativo</span><span class="sxs-lookup"><span data-stu-id="0ed62-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="0ed62-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="0ed62-115">0x0001</span></span> | <span data-ttu-id="0ed62-116">Defina como 1 se o modo nativo; 0 se o modo alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="0ed62-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="0ed62-117">TF \_ CONversãomode \_ katakana</span><span class="sxs-lookup"><span data-stu-id="0ed62-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="0ed62-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="0ed62-118">0x0002</span></span> | <span data-ttu-id="0ed62-119">Defina como 1 se modo KATAKANA; 0 se o modo HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="0ed62-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="0ed62-120">TF \_ CONversãomode \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="0ed62-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="0ed62-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="0ed62-121">0x0008</span></span> | <span data-ttu-id="0ed62-122">Defina como 1 se modo de forma completa; 0 se o modo de meia forma.</span><span class="sxs-lookup"><span data-stu-id="0ed62-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="0ed62-123">TF \_ CONversãomode \_ Roman</span><span class="sxs-lookup"><span data-stu-id="0ed62-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="0ed62-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="0ed62-124">0x0010</span></span> | <span data-ttu-id="0ed62-125">Defina como 1 para impedir o processamento de conversões por IME; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="0ed62-126">TF \_ CONversionmode \_ charCode</span><span class="sxs-lookup"><span data-stu-id="0ed62-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="0ed62-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="0ed62-127">0x0020</span></span> | <span data-ttu-id="0ed62-128">Defina como 1 se o modo de entrada de código de caractere; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="0ed62-129">TF \_ CONversãomode \_ SOFTKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="0ed62-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="0ed62-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="0ed62-130">0x0080</span></span> | <span data-ttu-id="0ed62-131">Defina como 1 se o modo de teclado virtual; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="0ed62-132">TF \_ CONversãomode \_ noConversion</span><span class="sxs-lookup"><span data-stu-id="0ed62-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="0ed62-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="0ed62-133">0x0100</span></span> | <span data-ttu-id="0ed62-134">Defina como 1 para impedir o processamento de conversões por IME; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="0ed62-135">TF \_ símbolo de CONversãomode \_</span><span class="sxs-lookup"><span data-stu-id="0ed62-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="0ed62-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="0ed62-136">0x0400</span></span> | <span data-ttu-id="0ed62-137">Defina como 1 se modo de conversão de símbolo; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="0ed62-138">TF \_ CONversãomode \_ corrigido</span><span class="sxs-lookup"><span data-stu-id="0ed62-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="0ed62-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="0ed62-139">0x0800</span></span> | <span data-ttu-id="0ed62-140">Defina como 1 se o modo de conversão fixa; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="0ed62-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="0ed62-141">Os valores a seguir são usados como um valor [de \_ compartimento de GUID \_ teclado \_ InputMode \_ ](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="0ed62-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="0ed62-142">Isso é equivalente a valores de [ \_ SMODE do IME](../intl/ime-composition-string-values.md) para IMM32.</span><span class="sxs-lookup"><span data-stu-id="0ed62-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="0ed62-143">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="0ed62-143">Flag</span></span>                            | <span data-ttu-id="0ed62-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0ed62-144">Value</span></span>  | <span data-ttu-id="0ed62-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ed62-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="0ed62-146">TF \_ sentençamode \_ None</span><span class="sxs-lookup"><span data-stu-id="0ed62-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="0ed62-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="0ed62-147">0x0000</span></span> | <span data-ttu-id="0ed62-148">Nenhuma informação para frase.</span><span class="sxs-lookup"><span data-stu-id="0ed62-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="0ed62-149">TF \_ sentençamode \_ PLAURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="0ed62-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="0ed62-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="0ed62-150">0x0001</span></span> | <span data-ttu-id="0ed62-151">O IME usa as informações de cláusula plural para executar o processamento de conversão.</span><span class="sxs-lookup"><span data-stu-id="0ed62-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="0ed62-152">TF \_ sentençamode \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="0ed62-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="0ed62-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="0ed62-153">0x0002</span></span> | <span data-ttu-id="0ed62-154">O IME executa o processamento de conversão no modo de caractere único.</span><span class="sxs-lookup"><span data-stu-id="0ed62-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="0ed62-155">TF \_ sentençamode \_ automático</span><span class="sxs-lookup"><span data-stu-id="0ed62-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="0ed62-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="0ed62-156">0x0004</span></span> | <span data-ttu-id="0ed62-157">O IME executa o processamento de conversão no modo automático.</span><span class="sxs-lookup"><span data-stu-id="0ed62-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="0ed62-158">TF \_ sentençamode \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="0ed62-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="0ed62-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="0ed62-159">0x0008</span></span> | <span data-ttu-id="0ed62-160">O IME usa informações de frase para prever o próximo caractere.</span><span class="sxs-lookup"><span data-stu-id="0ed62-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="0ed62-161">\_conversa TF sentençamode \_</span><span class="sxs-lookup"><span data-stu-id="0ed62-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="0ed62-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="0ed62-162">0x0010</span></span> | <span data-ttu-id="0ed62-163">O IME usa o modo de conversa.</span><span class="sxs-lookup"><span data-stu-id="0ed62-163">The IME uses conversation mode.</span></span> <span data-ttu-id="0ed62-164">Isso é útil para aplicativos de chat.</span><span class="sxs-lookup"><span data-stu-id="0ed62-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="0ed62-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed62-165">Requirements</span></span>



| <span data-ttu-id="0ed62-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed62-166">Requirement</span></span> | <span data-ttu-id="0ed62-167">Valor</span><span class="sxs-lookup"><span data-stu-id="0ed62-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed62-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ed62-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed62-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ed62-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ed62-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ed62-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed62-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ed62-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0ed62-172">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0ed62-172">Redistributable</span></span><br/>          | <span data-ttu-id="0ed62-173">TSF 1,0 onwindows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98</span><span class="sxs-lookup"><span data-stu-id="0ed62-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="0ed62-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ed62-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ed62-175"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed62-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ed62-176">INSERI</span><span class="sxs-lookup"><span data-stu-id="0ed62-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ed62-177"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ed62-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed62-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ed62-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed62-179">Compartimentos predefinidos</span><span class="sxs-lookup"><span data-stu-id="0ed62-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

