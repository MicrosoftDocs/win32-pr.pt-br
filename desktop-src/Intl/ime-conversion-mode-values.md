---
description: Examine a lista de valores do modo de conversão do IME (editor de método de entrada). Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores do modo de conversão do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406749"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="736a3-104">Valores do modo de conversão do IME</span><span class="sxs-lookup"><span data-stu-id="736a3-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="736a3-105">Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="736a3-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="736a3-106">bit</span><span class="sxs-lookup"><span data-stu-id="736a3-106">Bit</span></span>                      | <span data-ttu-id="736a3-107">Significado</span><span class="sxs-lookup"><span data-stu-id="736a3-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="736a3-108">\_CMODE \_ alfanumérico do IME</span><span class="sxs-lookup"><span data-stu-id="736a3-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="736a3-109">Modo de entrada alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="736a3-109">Alphanumeric input mode.</span></span> <span data-ttu-id="736a3-110">Esse é o padrão, definido como 0x0000.</span><span class="sxs-lookup"><span data-stu-id="736a3-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="736a3-111">\_charco de CMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="736a3-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="736a3-112">Defina como 1 se o modo de entrada de código de caractere; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="736a3-113">\_CMODE \_ EUDC do IME</span><span class="sxs-lookup"><span data-stu-id="736a3-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="736a3-114">Defina como 1 se modo de conversão EUDC; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="736a3-115">CMODE do IME \_ \_ corrigido</span><span class="sxs-lookup"><span data-stu-id="736a3-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="736a3-116">**Windows me/98, windows 2000, Windows XP:** Defina como 1 se o modo de conversão fixa; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="736a3-117">\_CMODE IME \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="736a3-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="736a3-118">Defina como 1 se modo de forma completa; 0 se o modo de meia forma.</span><span class="sxs-lookup"><span data-stu-id="736a3-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="736a3-119">\_CMODE IME \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="736a3-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="736a3-120">Defina como 1 se o modo de conversão em HANJA; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="736a3-121">IME \_ CMODE \_ katakana</span><span class="sxs-lookup"><span data-stu-id="736a3-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="736a3-122">Defina como 1 se modo KATAKANA; 0 se o modo HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="736a3-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="736a3-123">IME \_ CMODE \_ nativo</span><span class="sxs-lookup"><span data-stu-id="736a3-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="736a3-124">Defina como 1 se o modo nativo; 0 se o modo alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="736a3-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="736a3-125">IME \_ CMODE \_ noConversion</span><span class="sxs-lookup"><span data-stu-id="736a3-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="736a3-126">Defina como 1 para impedir o processamento de conversões por IME; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="736a3-127">IME \_ CMODE \_ Romano</span><span class="sxs-lookup"><span data-stu-id="736a3-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="736a3-128">Defina como 1 se modo de entrada ROMAN; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="736a3-129">\_CMODE IME \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="736a3-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="736a3-130">Defina como 1 se o modo de teclado virtual; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="736a3-131">\_símbolo de CMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="736a3-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="736a3-132">Defina como 1 se modo de conversão de símbolo; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="736a3-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="736a3-133">Todos os outros bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="736a3-133">All other bits are reserved.</span></span>

 

 



