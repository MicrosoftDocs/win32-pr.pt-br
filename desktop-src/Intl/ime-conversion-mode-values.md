---
description: Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valores do modo de conversão do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090666"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="b5679-103">Valores do modo de conversão do IME</span><span class="sxs-lookup"><span data-stu-id="b5679-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="b5679-104">Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="b5679-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="b5679-105">bit</span><span class="sxs-lookup"><span data-stu-id="b5679-105">Bit</span></span>                      | <span data-ttu-id="b5679-106">Significado</span><span class="sxs-lookup"><span data-stu-id="b5679-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5679-107">\_CMODE \_ alfanumérico do IME</span><span class="sxs-lookup"><span data-stu-id="b5679-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="b5679-108">Modo de entrada alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="b5679-108">Alphanumeric input mode.</span></span> <span data-ttu-id="b5679-109">Esse é o padrão, definido como 0x0000.</span><span class="sxs-lookup"><span data-stu-id="b5679-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="b5679-110">\_charco de CMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="b5679-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="b5679-111">Defina como 1 se o modo de entrada de código de caractere; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="b5679-112">\_CMODE \_ EUDC do IME</span><span class="sxs-lookup"><span data-stu-id="b5679-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="b5679-113">Defina como 1 se modo de conversão EUDC; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="b5679-114">CMODE do IME \_ \_ corrigido</span><span class="sxs-lookup"><span data-stu-id="b5679-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="b5679-115">**Windows me/98, windows 2000, Windows XP:** Defina como 1 se o modo de conversão fixa; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="b5679-116">\_CMODE IME \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="b5679-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="b5679-117">Defina como 1 se modo de forma completa; 0 se o modo de meia forma.</span><span class="sxs-lookup"><span data-stu-id="b5679-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="b5679-118">\_CMODE IME \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="b5679-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="b5679-119">Defina como 1 se o modo de conversão em HANJA; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="b5679-120">IME \_ CMODE \_ katakana</span><span class="sxs-lookup"><span data-stu-id="b5679-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="b5679-121">Defina como 1 se modo KATAKANA; 0 se o modo HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="b5679-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="b5679-122">IME \_ CMODE \_ nativo</span><span class="sxs-lookup"><span data-stu-id="b5679-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="b5679-123">Defina como 1 se o modo nativo; 0 se o modo alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="b5679-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="b5679-124">IME \_ CMODE \_ noConversion</span><span class="sxs-lookup"><span data-stu-id="b5679-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="b5679-125">Defina como 1 para impedir o processamento de conversões por IME; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="b5679-126">IME \_ CMODE \_ Romano</span><span class="sxs-lookup"><span data-stu-id="b5679-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="b5679-127">Defina como 1 se modo de entrada ROMAN; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="b5679-128">\_CMODE IME \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="b5679-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="b5679-129">Defina como 1 se o modo de teclado virtual; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="b5679-130">\_símbolo de CMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="b5679-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="b5679-131">Defina como 1 se modo de conversão de símbolo; 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="b5679-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="b5679-132">Todos os outros bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="b5679-132">All other bits are reserved.</span></span>

 

 



