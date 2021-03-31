---
title: Erros de mciSendString
description: Erros de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR valores de retorno, erros de mciSendString
- referência de multimídia, erros de mciSendString
- referência para multimídia, erros de mciSendString
- MCI (interface de controle de mídia), erros de mciSendString
- MCI (interface de controle de mídia), erros de mciSendString
- referência para MCI, erros de mciSendString
- Referência de MCI, erros de mciSendString
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- erros de mciSendString
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823729"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="95897-116">Erros de mciSendString</span><span class="sxs-lookup"><span data-stu-id="95897-116">mciSendString Errors</span></span>

<span data-ttu-id="95897-117">Os erros a seguir são retornados pela função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , mas não por [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="95897-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="95897-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95897-118">Value</span></span>                             | <span data-ttu-id="95897-119">Significado</span><span class="sxs-lookup"><span data-stu-id="95897-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="95897-120">\_constante MCIERR inadequada \_</span><span class="sxs-lookup"><span data-stu-id="95897-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="95897-121">O valor especificado para um parâmetro é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="95897-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="95897-122">MCIERR \_ inteiro inválido \_</span><span class="sxs-lookup"><span data-stu-id="95897-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="95897-123">Um inteiro no comando era inválido ou estava ausente.</span><span class="sxs-lookup"><span data-stu-id="95897-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="95897-124">MCIERR \_ sinalizadores duplicados \_</span><span class="sxs-lookup"><span data-stu-id="95897-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="95897-125">Um sinalizador ou valor foi especificado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="95897-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="95897-126">MCIERR \_ \_ cadeia de caracteres de comando ausente \_</span><span class="sxs-lookup"><span data-stu-id="95897-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="95897-127">Nenhum comando foi especificado.</span><span class="sxs-lookup"><span data-stu-id="95897-127">No command was specified.</span></span>                         |
| <span data-ttu-id="95897-128">MCIERR \_ \_ nome do dispositivo ausente \_</span><span class="sxs-lookup"><span data-stu-id="95897-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="95897-129">Nenhum nome de dispositivo foi especificado.</span><span class="sxs-lookup"><span data-stu-id="95897-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="95897-130">MCIERR \_ \_ argumento de cadeia de caracteres ausente \_</span><span class="sxs-lookup"><span data-stu-id="95897-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="95897-131">Um valor de cadeia de caracteres estava ausente no comando.</span><span class="sxs-lookup"><span data-stu-id="95897-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="95897-132">MCIERR \_ New \_ requer \_ alias</span><span class="sxs-lookup"><span data-stu-id="95897-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="95897-133">Um alias deve ser usado com o nome do dispositivo "novo".</span><span class="sxs-lookup"><span data-stu-id="95897-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="95897-134">MCIERR \_ sem \_ aspas de fechamento \_</span><span class="sxs-lookup"><span data-stu-id="95897-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="95897-135">Está faltando um sinal de aspas de fechamento.</span><span class="sxs-lookup"><span data-stu-id="95897-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="95897-136">MCIERR \_ notificar \_ ao \_ \_ abrir automaticamente</span><span class="sxs-lookup"><span data-stu-id="95897-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="95897-137">O sinalizador "Notify" é inválido com a abertura automática.</span><span class="sxs-lookup"><span data-stu-id="95897-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="95897-138">\_estouro de param MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="95897-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="95897-139">A cadeia de caracteres de saída não era longa o suficiente.</span><span class="sxs-lookup"><span data-stu-id="95897-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="95897-140">MCIERR do \_ analisador \_ interno</span><span class="sxs-lookup"><span data-stu-id="95897-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="95897-141">Ocorreu um erro interno do analisador.</span><span class="sxs-lookup"><span data-stu-id="95897-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="95897-142">MCIERR \_ \_ palavra-chave não reconhecida</span><span class="sxs-lookup"><span data-stu-id="95897-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="95897-143">Um parâmetro de comando desconhecido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="95897-143">An unknown command parameter was specified.</span></span>       |



 

 

 