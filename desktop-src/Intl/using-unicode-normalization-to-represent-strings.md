---
description: Os aplicativos podem usar Unicode para representar cadeias de caracteres em vários formulários.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Usando a normalização Unicode para representar cadeias de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837416"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="c33fe-103">Usando a normalização Unicode para representar cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="c33fe-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="c33fe-104">Os aplicativos podem usar Unicode para representar cadeias de caracteres em vários formulários.</span><span class="sxs-lookup"><span data-stu-id="c33fe-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="c33fe-105">À medida que a aceitação Unicode cresceu, especialmente pela Internet, a necessidade foi surgida para eliminar diferenças não essenciais em cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c33fe-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="c33fe-106">Várias representações para uma combinação de caracteres complicam o software, por exemplo, quando um servidor Web responde a uma solicitação de página ou um vinculador procura um identificador específico em uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c33fe-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="c33fe-107">Diferentes cadeias de caracteres Unicode podem parecer visualmente idênticas, gerando preocupações de segurança.</span><span class="sxs-lookup"><span data-stu-id="c33fe-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="c33fe-108">Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="c33fe-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="c33fe-109">Em resposta a esse requisito, o consórcio Unicode definiu um processo chamado "normalização", que produz uma representação binária para qualquer uma das representações binárias equivalentes de um caractere.</span><span class="sxs-lookup"><span data-stu-id="c33fe-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="c33fe-110">Depois de normalizado, duas cadeias de caracteres serão equivalentes se e somente se tiverem representações binárias idênticas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="c33fe-111">A normalização elimina algumas diferenças, mas preserva maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="c33fe-112">Para usar a normalização Unicode, um aplicativo pode chamar as funções [**normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) para reorganização das cadeias de caracteres ACCCORDING para Unicode 4,0 TR \# 15.</span><span class="sxs-lookup"><span data-stu-id="c33fe-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="c33fe-113">A normalização pode ajudar a melhorar a segurança, reduzindo representações de cadeias de caracteres alternativas que têm o mesmo significado linguístico.</span><span class="sxs-lookup"><span data-stu-id="c33fe-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="c33fe-114">Lembre-se, no entanto, que a normalização não pode eliminar totalmente as representações alternativas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="c33fe-115">Para obter uma descrição detalhada dos padrões Unicode para normalização, consulte [Unicode padrão do anexo \# 15: formulários de normalização Unicode](https://www.unicode.org/reports/tr15) (UAX \# 15).</span><span class="sxs-lookup"><span data-stu-id="c33fe-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="c33fe-116">Como a normalização pode alterar a forma de uma cadeia de caracteres, mecanismos de segurança ou algoritmos de validação de caracteres normalmente devem ser implementados após a normalização.</span><span class="sxs-lookup"><span data-stu-id="c33fe-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="c33fe-117">Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="c33fe-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="c33fe-118">Fornecer várias representações da mesma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c33fe-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="c33fe-119">Em muitos casos, o Unicode permite várias representações do que é, lingüísticamente, a mesma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c33fe-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="c33fe-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c33fe-120">For example:</span></span>

-   <span data-ttu-id="c33fe-121">A maiúscula A com trema (trem) pode ser representada como um único ponto de código Unicode "Ä" (U + 00C4) ou a combinação de maiúscula A e combinação de caracteres de trema ("A" + "̈", ou seja, U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="c33fe-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="c33fe-122">As considerações semelhantes se aplicam a muitos outros caracteres com marcas de sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="c33fe-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="c33fe-123">A própria capital pode ser representada da maneira usual (letra latina maiúscula A, U + 0041) ou por letra minúscula latina maiúscula A (U + FF21).</span><span class="sxs-lookup"><span data-stu-id="c33fe-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="c33fe-124">As considerações semelhantes se aplicam às outras letras latinas simples (maiúsculas e minúsculas) e aos caracteres Katakana usados na escrita de japonês.</span><span class="sxs-lookup"><span data-stu-id="c33fe-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="c33fe-125">A cadeia de caracteres "fi" pode ser representada pelos caracteres "f" e "i" (U + 0066 U + 0069) ou pela ligadura "fi" (U + FB01).</span><span class="sxs-lookup"><span data-stu-id="c33fe-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="c33fe-126">Considerações semelhantes se aplicam a muitas outras combinações de caracteres para os quais o Unicode define ligaturas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="c33fe-127">Usar os quatro formulários de normalização definidos</span><span class="sxs-lookup"><span data-stu-id="c33fe-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="c33fe-128">Seus aplicativos podem executar a normalização Unicode usando vários algoritmos, chamados de "formas de normalização", que obedecem a diferentes regras.</span><span class="sxs-lookup"><span data-stu-id="c33fe-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="c33fe-129">O consórcio Unicode definiu quatro formas de normalização: NFC (forma C), NFD (forma D), NFKC (Form KC) e NFKD (Form KD).</span><span class="sxs-lookup"><span data-stu-id="c33fe-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="c33fe-130">Cada formulário elimina algumas diferenças, mas preserva maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="c33fe-131">O Win32 e o .NET Framework dão suporte a todos os quatro formulários de normalização.</span><span class="sxs-lookup"><span data-stu-id="c33fe-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="c33fe-132">O [**\_ formulário**](/windows/desktop/api/Winnls/ne-winnls-norm_form) normal de tipo de enumeração NLS dá suporte aos quatro formulários de normalização Unicode padrão.</span><span class="sxs-lookup"><span data-stu-id="c33fe-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="c33fe-133">Os formulários C e D fornecem formulários canônicos para cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c33fe-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="c33fe-134">As formas não canônicas KC e KD fornecem compatibilidade adicional e podem revelar determinadas equivalências semânticas que não são aparentes nos formulários C e D. No entanto, eles fazem isso às custas de uma certa perda de informações e geralmente não devem ser usados como uma forma canônica de armazenar cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c33fe-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="c33fe-135">Das duas formas canônicas, o formulário C é um formulário "composto" e o formulário D é um formulário "decomposto".</span><span class="sxs-lookup"><span data-stu-id="c33fe-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="c33fe-136">Por exemplo, o formulário C usa o único ponto de código Unicode "Ä" (U + 00C4), enquanto o formato D usa ("A" + "̈", que é U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="c33fe-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="c33fe-137">Elas são processadas de forma idêntica, pois "̈" (U + 0308) é um caractere de combinação.</span><span class="sxs-lookup"><span data-stu-id="c33fe-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="c33fe-138">O formulário D pode usar qualquer número de pontos de código para representar um único ponto de código usado pelo formulário C.</span><span class="sxs-lookup"><span data-stu-id="c33fe-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="c33fe-139">Se duas cadeias de caracteres forem idênticas nas formas C ou D, elas serão idênticas no outro formulário.</span><span class="sxs-lookup"><span data-stu-id="c33fe-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="c33fe-140">Além disso, quando renderizado corretamente, eles são exibidos de forma indistinguíveis uns dos outros e da cadeia de caracteres não normalizada original.</span><span class="sxs-lookup"><span data-stu-id="c33fe-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="c33fe-141">Depois de normalizadas, as cadeias de caracteres não podem ser retornadas consistentemente para sua representação original.</span><span class="sxs-lookup"><span data-stu-id="c33fe-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="c33fe-142">Por exemplo, se uma cadeia de caracteres com uma mistura de representações de caracteres compostas e decompostas for convertida em uma forma normalizada, não haverá nenhuma maneira de desnormalizar a cadeia de caracteres mista original.</span><span class="sxs-lookup"><span data-stu-id="c33fe-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="c33fe-143">Portanto, se um aplicativo exigir a representação original da cadeia de caracteres, ele deverá armazenar essa representação explicitamente.</span><span class="sxs-lookup"><span data-stu-id="c33fe-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="c33fe-144">No entanto, a conversão entre os dois formulários canônicos é reversível.</span><span class="sxs-lookup"><span data-stu-id="c33fe-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="c33fe-145">Uma cadeia de caracteres no formato C pode ser convertida para o formulário D e, em seguida, de volta para o formulário C, e o resultado é idêntico ao formato original da cadeia C.</span><span class="sxs-lookup"><span data-stu-id="c33fe-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="c33fe-146">Os formulários KC e KD são semelhantes aos formulários C e D, respectivamente, mas essas "formas de compatibilidade" têm mapeamentos adicionais de caracteres compatíveis para a forma básica de cada caractere.</span><span class="sxs-lookup"><span data-stu-id="c33fe-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="c33fe-147">Esses mapeamentos podem causar a perda de variações de caracteres secundárias.</span><span class="sxs-lookup"><span data-stu-id="c33fe-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="c33fe-148">Eles combinam determinados caracteres que são visualmente distintos.</span><span class="sxs-lookup"><span data-stu-id="c33fe-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="c33fe-149">Por exemplo, eles combinam caracteres de largura inteira e de meia largura com o mesmo significado semântico, ou formas diferentes da mesma letra árabe, ou a Ligadura "fi" (U + FB01) e o par de caracteres "fi" (U + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="c33fe-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="c33fe-150">Eles também combinam alguns caracteres que às vezes podem ter um significado semântico diferente, como um dígito escrito como um sobrescrito, como subscrito ou colocado em um círculo.</span><span class="sxs-lookup"><span data-stu-id="c33fe-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="c33fe-151">Devido a essa perda de informações, os formulários KC e KD geralmente não devem ser usados como formas canônicas de cadeias de caracteres, mas são úteis para determinados aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c33fe-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="c33fe-152">O formulário KC é um formulário composto e o formulário KD é um formulário decomposto.</span><span class="sxs-lookup"><span data-stu-id="c33fe-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="c33fe-153">O aplicativo pode voltar entre os formulários KC e KD, mas não há uma maneira consistente de ir de forma KC ou KD de volta para a cadeia de caracteres original, mesmo que a cadeia de caracteres original esteja no formato C ou D.</span><span class="sxs-lookup"><span data-stu-id="c33fe-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="c33fe-154">O Windows, os aplicativos da Microsoft e o .NET Framework geralmente geram caracteres na forma C usando métodos de entrada normais.</span><span class="sxs-lookup"><span data-stu-id="c33fe-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="c33fe-155">Para a maioria dos fins no Windows, o formulário C é o formulário preferido.</span><span class="sxs-lookup"><span data-stu-id="c33fe-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="c33fe-156">Por exemplo, os caracteres no formato C são produzidos pela entrada de teclado do Windows.</span><span class="sxs-lookup"><span data-stu-id="c33fe-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="c33fe-157">No entanto, os caracteres importados da Web e de outras plataformas podem introduzir outros formulários de normalização no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c33fe-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="c33fe-158">Os exemplos a seguir são desenhados a partir de UAX \# 15 e ilustram as diferenças entre os quatro formulários de normalização.</span><span class="sxs-lookup"><span data-stu-id="c33fe-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c33fe-159">Original</span><span class="sxs-lookup"><span data-stu-id="c33fe-159">Original</span></span></th>
<th><span data-ttu-id="c33fe-160">Formulário D</span><span class="sxs-lookup"><span data-stu-id="c33fe-160">Form D</span></span></th>
<th><span data-ttu-id="c33fe-161">Formulário C</span><span class="sxs-lookup"><span data-stu-id="c33fe-161">Form C</span></span></th>
<th><span data-ttu-id="c33fe-162">Observações</span><span class="sxs-lookup"><span data-stu-id="c33fe-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c33fe-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="c33fe-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="c33fe-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="c33fe-166">O ffi_ligature (U + FB03) não é decomposto, pois tem um mapeamento de compatibilidade, não um mapeamento canônico. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="c33fe-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="c33fe-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="c33fe-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="c33fe-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="c33fe-173">O NUMERAL Romano IV (U + 2163) não é decomposto. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="c33fe-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="c33fe-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-177">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-177">ga</span></span></td>
<td><span data-ttu-id="c33fe-178">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-178">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-179">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="c33fe-180">Diferentes equivalentes de compatibilidade de um único caractere japonês não resultam na mesma cadeia de caracteres no formato C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-181">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-181">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-182">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-182">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-183">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-187">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-188">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-189">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-190">hw_ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-191">hw_ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-192">hw_ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-193">kaks</span><span class="sxs-lookup"><span data-stu-id="c33fe-193">kaks</span></span></td>
<td><span data-ttu-id="c33fe-194">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="c33fe-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="c33fe-195">kaks</span><span class="sxs-lookup"><span data-stu-id="c33fe-195">kaks</span></span></td>
<td><span data-ttu-id="c33fe-196">As sílabas Hangul são mantidas sob normalização.</span><span class="sxs-lookup"><span data-stu-id="c33fe-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c33fe-197">Original</span><span class="sxs-lookup"><span data-stu-id="c33fe-197">Original</span></span></th>
<th><span data-ttu-id="c33fe-198">Formulário KD</span><span class="sxs-lookup"><span data-stu-id="c33fe-198">Form KD</span></span></th>
<th><span data-ttu-id="c33fe-199">Formulário KC</span><span class="sxs-lookup"><span data-stu-id="c33fe-199">Form KC</span></span></th>
<th><span data-ttu-id="c33fe-200">Observações</span><span class="sxs-lookup"><span data-stu-id="c33fe-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c33fe-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="c33fe-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="c33fe-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="c33fe-204">O ffi_ligature (U + FB03) é decomposto no formato KC, mas não no formato C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="c33fe-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="c33fe-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="c33fe-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="c33fe-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="c33fe-211">As cadeias de caracteres resultantes aqui são idênticas no formato KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="c33fe-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="c33fe-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="c33fe-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-215">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-215">ga</span></span></td>
<td><span data-ttu-id="c33fe-216">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-216">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-217">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="c33fe-218">Diferentes equivalentes de compatibilidade de um único caractere japonês resultam na mesma cadeia de caracteres no formato KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c33fe-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-219">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-219">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-220">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-220">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-221">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-223">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-223">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-224">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-225">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="c33fe-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="c33fe-226">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-226">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-227">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c33fe-228">hw_ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-229">Ka + dez</span><span class="sxs-lookup"><span data-stu-id="c33fe-229">ka +ten</span></span></td>
<td><span data-ttu-id="c33fe-230">ga</span><span class="sxs-lookup"><span data-stu-id="c33fe-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c33fe-231">kaks</span><span class="sxs-lookup"><span data-stu-id="c33fe-231">kaks</span></span></td>
<td><span data-ttu-id="c33fe-232">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="c33fe-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="c33fe-233">kaks</span><span class="sxs-lookup"><span data-stu-id="c33fe-233">kaks</span></span></td>
<td><span data-ttu-id="c33fe-234">As sílabas Hangul são mantidas sob normalização.</span><span class="sxs-lookup"><span data-stu-id="c33fe-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="c33fe-235">Em versões anteriores do Unicode, caracteres Jamo como KS <sub>f</sub> tinham mapeamentos de compatibilidade para k <sub>f</sub> + s <sub>f</sub>.</span><span class="sxs-lookup"><span data-stu-id="c33fe-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="c33fe-236">Esses mapeamentos foram removidos em 2.1.9 Unicode para garantir que as sílabas Hangul sejam mantidas.</span><span class="sxs-lookup"><span data-stu-id="c33fe-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="c33fe-237">As duas tabelas acima têm direitos autorais de © 1998-2006 Unicode, Inc. Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="c33fe-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="c33fe-238">Usar formulários compostos para glifos únicos</span><span class="sxs-lookup"><span data-stu-id="c33fe-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="c33fe-239">Muitas sequências de caracteres que correspondem a um único glifo não têm formulários compostos.</span><span class="sxs-lookup"><span data-stu-id="c33fe-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="c33fe-240">Mesmo quando normalizado pela forma C, um único glifo Visual ou elemento de texto lógico pode ser composto por vários pontos de código Unicode.</span><span class="sxs-lookup"><span data-stu-id="c33fe-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="c33fe-241">Por exemplo, vários caracteres usados na escrita de lituano têm diacríticos duplos, pois têm apenas formulários decompostos.</span><span class="sxs-lookup"><span data-stu-id="c33fe-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="c33fe-242">Um exemplo é minúscula U com Macron e til ("ū̃", U + 016B U + 0303, em que o primeiro ponto de código é um U minúsculo com Macron e o segundo é um acento agudo combinável).</span><span class="sxs-lookup"><span data-stu-id="c33fe-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="c33fe-243">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c33fe-243">Example</span></span>

<span data-ttu-id="c33fe-244">Um exemplo relevante pode ser encontrado em [NLS: exemplo de normalização Unicode](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c33fe-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c33fe-245">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c33fe-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c33fe-246">Usando o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="c33fe-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="c33fe-247">Considerações sobre segurança: recursos internacionais</span><span class="sxs-lookup"><span data-stu-id="c33fe-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="c33fe-248">**IsNormalizedString**</span><span class="sxs-lookup"><span data-stu-id="c33fe-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="c33fe-249">**Normalizestring**</span><span class="sxs-lookup"><span data-stu-id="c33fe-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




