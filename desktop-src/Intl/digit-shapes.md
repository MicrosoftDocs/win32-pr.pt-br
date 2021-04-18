---
description: O árabe e muitos outros idiomas têm formas clássicas para números que são diferentes dos dígitos ocidentais convencionais mais frequentemente usados nos computadores.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formas de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756917"
---
# <a name="digit-shapes"></a><span data-ttu-id="778b6-103">Formas de dígitos</span><span class="sxs-lookup"><span data-stu-id="778b6-103">Digit Shapes</span></span>

<span data-ttu-id="778b6-104">O árabe e muitos outros idiomas têm formas clássicas para números que são diferentes dos dígitos ocidentais convencionais mais frequentemente usados nos computadores.</span><span class="sxs-lookup"><span data-stu-id="778b6-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="778b6-105">Para evitar ambigüidade ao nomear essas formas, este documento usa os seguintes nomes do padrão Unicode.</span><span class="sxs-lookup"><span data-stu-id="778b6-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="778b6-106">Nome Unicode dos dígitos</span><span class="sxs-lookup"><span data-stu-id="778b6-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="778b6-107">País/região onde usado</span><span class="sxs-lookup"><span data-stu-id="778b6-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="778b6-108">Dígitos europeus</span><span class="sxs-lookup"><span data-stu-id="778b6-108">European digits</span></span>                                                | <span data-ttu-id="778b6-109">Europa, Américas e muitos outros países/regiões</span><span class="sxs-lookup"><span data-stu-id="778b6-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="778b6-110">Arabic-Indic dígitos</span><span class="sxs-lookup"><span data-stu-id="778b6-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="778b6-111">Países/regiões árabes (embora muitos usem dígitos europeus)</span><span class="sxs-lookup"><span data-stu-id="778b6-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="778b6-112">Outros dígitos nacionais: dígitos índicos, dígitos tailandeses e semelhantes</span><span class="sxs-lookup"><span data-stu-id="778b6-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="778b6-113">Vários países/regiões</span><span class="sxs-lookup"><span data-stu-id="778b6-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="778b6-114">O Unicode fornece pontos de código separados para cada forma de dígito.</span><span class="sxs-lookup"><span data-stu-id="778b6-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="778b6-115">Portanto, para acessar formas especiais de dígitos de idioma, seu aplicativo pode usar os códigos de caracteres Unicode relevantes para os dígitos acima, U + 0030 até U + 0039.</span><span class="sxs-lookup"><span data-stu-id="778b6-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="778b6-116">Esses códigos são sempre exibidos com a forma apropriada, sujeito à disponibilidade da fonte.</span><span class="sxs-lookup"><span data-stu-id="778b6-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="778b6-117">Os códigos de caractere Unicode U + 0030 a U + 0039 representam nominalmente os dígitos europeus de 0 a 9, mas sua forma de dígito pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="778b6-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="778b6-118">As APIs de texto GDI e DirectWrite fornecem mecanismos para que os aplicativos controlem esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="778b6-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="778b6-119">(Consulte, por exemplo, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) ou [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) O comportamento em alguns controles do Shell e estruturas de interface do usuário pode responder às configurações de localidade do usuário para substituição de dígitos; a [localidade \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE pode ser usada para obter as configurações de substituição de dígitos padrão para localidades diferentes ou para as configurações de área de trabalho do usuário atual para substituição de dígitos.</span><span class="sxs-lookup"><span data-stu-id="778b6-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="778b6-120">Dígitos nativos</span><span class="sxs-lookup"><span data-stu-id="778b6-120">Native Digits</span></span>

<span data-ttu-id="778b6-121">Os dígitos nativos são as formas de dígitos escolhidas pelo usuário na folha de propriedades **número** na parte opções regionais e de idiomas do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="778b6-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="778b6-122">Para localizar a apresentação de dígitos preferida pelo usuário, seu aplicativo usa a função [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante de [localidade \_ SNATIVEDIGITS](locale-snative-constants.md) que representa as informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="778b6-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="778b6-123">Normalmente, os códigos de dígitos Unicode são gerados em rotinas do sistema operacional de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="778b6-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="778b6-124">Portanto, os sistemas operacionais de tempo de execução comuns devem ser atualizados para que o aplicativo Inspecione a [localidade \_ SNATIVEDIGITS](locale-snative-constants.md) apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="778b6-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="778b6-125">Substituição de dígitos</span><span class="sxs-lookup"><span data-stu-id="778b6-125">Digit Substitution</span></span>

<span data-ttu-id="778b6-126">O aplicativo pode usar a substituição de dígitos para informar ao sistema operacional como imprimir dígitos U + 0030 até U + 0039.</span><span class="sxs-lookup"><span data-stu-id="778b6-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="778b6-127">A [constante \_ IDIGITSUBSTITUTION de localidade](locale-idigitsubstitution.md) controla essa operação.</span><span class="sxs-lookup"><span data-stu-id="778b6-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="778b6-128">Formatação de dígitos para uma única função</span><span class="sxs-lookup"><span data-stu-id="778b6-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="778b6-129">As funções de [ \_ resultados](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)e GCP têm sinalizadores que regem a substituição de códigos Unicode U + 0030 por u + 0039 durante a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="778b6-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="778b6-130">Esses sinalizadores substituem as configurações regionais no painel de controle, mas não redefinem as configurações.</span><span class="sxs-lookup"><span data-stu-id="778b6-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="778b6-131">Além disso, eles não substituem os códigos Unicode NADS e nós nesta.</span><span class="sxs-lookup"><span data-stu-id="778b6-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="778b6-132">Os sinalizadores a seguir estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="778b6-132">The following flags are available.</span></span>



| <span data-ttu-id="778b6-133">Flags</span><span class="sxs-lookup"><span data-stu-id="778b6-133">Flags</span></span>                 | <span data-ttu-id="778b6-134">Dígitos usados</span><span class="sxs-lookup"><span data-stu-id="778b6-134">Digits used</span></span>                      | <span data-ttu-id="778b6-135">Usado em</span><span class="sxs-lookup"><span data-stu-id="778b6-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="778b6-136">ETO \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="778b6-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="778b6-137">Dígitos europeus</span><span class="sxs-lookup"><span data-stu-id="778b6-137">European digits</span></span>                  | <span data-ttu-id="778b6-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="778b6-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="778b6-139">ETO \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="778b6-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="778b6-140">Dígitos apropriados para a localidade</span><span class="sxs-lookup"><span data-stu-id="778b6-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="778b6-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="778b6-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="778b6-142">GCP \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="778b6-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="778b6-143">Dígitos europeus</span><span class="sxs-lookup"><span data-stu-id="778b6-143">European digits</span></span>                  | <span data-ttu-id="778b6-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="778b6-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="778b6-145">GCP \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="778b6-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="778b6-146">Dígitos apropriados para a localidade</span><span class="sxs-lookup"><span data-stu-id="778b6-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="778b6-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="778b6-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="778b6-148">GCPCLASS \_ LATINNUMBER</span><span class="sxs-lookup"><span data-stu-id="778b6-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="778b6-149">Dígitos europeus</span><span class="sxs-lookup"><span data-stu-id="778b6-149">European digits</span></span>                  | <span data-ttu-id="778b6-150">**resultados do GCP \_**</span><span class="sxs-lookup"><span data-stu-id="778b6-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="778b6-151">GCPCLASS \_ LOCALNUMBER</span><span class="sxs-lookup"><span data-stu-id="778b6-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="778b6-152">Dígitos apropriados para a localidade</span><span class="sxs-lookup"><span data-stu-id="778b6-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="778b6-153">**resultados do GCP \_**</span><span class="sxs-lookup"><span data-stu-id="778b6-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="778b6-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="778b6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="778b6-155">Sobre o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="778b6-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="778b6-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="778b6-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="778b6-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="778b6-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
