---
title: Cadeias de caracteres
description: Esta seção discute as funções de cadeia de caracteres.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- recursos, cadeias de caracteres
- cadeias de caracteres
- funções de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642299"
---
# <a name="strings"></a><span data-ttu-id="5ca8f-106">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="5ca8f-106">Strings</span></span>

<span data-ttu-id="5ca8f-107">Esta seção descreve as funções de cadeia de caracteres e explica como usá-las em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="5ca8f-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5ca8f-108">In This Section</span></span>



| <span data-ttu-id="5ca8f-109">Nome</span><span class="sxs-lookup"><span data-stu-id="5ca8f-109">Name</span></span>                                     | <span data-ttu-id="5ca8f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ca8f-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="5ca8f-111">Sobre cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="5ca8f-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="5ca8f-112">Discute as funções de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="5ca8f-113">Sobre o strsafe. h</span><span class="sxs-lookup"><span data-stu-id="5ca8f-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="5ca8f-114">Discute as funções de cadeia de caracteres no strsafe. h.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="5ca8f-115">Referência de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="5ca8f-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="5ca8f-116">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="5ca8f-117">Funções de Cadeia de Caracteres</span><span class="sxs-lookup"><span data-stu-id="5ca8f-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ca8f-118">Nome</span><span class="sxs-lookup"><span data-stu-id="5ca8f-118">Name</span></span></th>
<th><span data-ttu-id="5ca8f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ca8f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ca8f-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-121">Converte uma cadeia de caracteres ou um único caractere em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="5ca8f-122">Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-124">Converte caracteres maiúsculos em um buffer para caracteres minúsculos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="5ca8f-125">A função converte os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-127">Recupera um ponteiro para o próximo caractere em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="5ca8f-128">Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-130">Recupera o ponteiro para o próximo caractere em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="5ca8f-131">Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-133">Recupera um ponteiro para o caractere anterior em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="5ca8f-134">Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-136">Recupera o ponteiro para o caractere anterior em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="5ca8f-137">Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-139">Traduz uma cadeia de caracteres no conjunto de caracteres definido pelo OEM.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-141">Converte um número especificado de caracteres em uma cadeia de caracteres no conjunto de caracteres definido pelo OEM.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-143">Converte uma cadeia de caracteres ou um único caractere em maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="5ca8f-144">Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-146">Converte caracteres minúsculos em um buffer em caracteres maiúsculos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="5ca8f-147">A função converte os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-149">Compara duas cadeias de caracteres, usando a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5ca8f-150">Para compatibilidade com Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> ou a versão Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-152">Compara duas cadeias de caracteres Unicode (caractere largo), usando a localidade especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-154">Mapeia uma cadeia de caracteres para outra, executando uma opção de transformação especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-156">Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="5ca8f-157">Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="5ca8f-158">Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-160">Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="5ca8f-161">Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="5ca8f-162">Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="5ca8f-163">Ao contrário de seus parentes <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> e <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, o <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exibe o comportamento padrão por meio do uso da opção <strong> # definir Unicode</strong> .</span><span class="sxs-lookup"><span data-stu-id="5ca8f-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="5ca8f-164">É a função recomendada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-166">Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="5ca8f-167">Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="5ca8f-168">Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-170">Determina se um caractere é um caractere alfabético.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="5ca8f-171">Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-173">Determina se um caractere é um caractere alfabético ou numérico.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="5ca8f-174">Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-176">Determina se um caractere é minúsculo.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="5ca8f-177">Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-179">Determina se um caractere é maiúsculo.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="5ca8f-180">Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Cadeia de caracteres LoadString</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-182">Carrega um recurso de cadeia de caracteres do arquivo executável associado a um módulo especificado, copia a cadeia de caracteres em um buffer e anexa um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-184">Acrescenta uma cadeia de caracteres a outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-186">Compara duas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-186">Compares two character strings.</span></span> <span data-ttu-id="5ca8f-187">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-189">Compara duas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-189">Compares two character strings.</span></span> <span data-ttu-id="5ca8f-190">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-192">Copia uma cadeia de caracteres em um buffer.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-194">Copia um número especificado de caracteres de uma cadeia de caracteres de origem em um buffer.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-196">Determina o comprimento da cadeia de caracteres especificada (não incluindo o caractere nulo de terminação).</span><span class="sxs-lookup"><span data-stu-id="5ca8f-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-198">Traduz uma cadeia de caracteres do conjunto de caracteres definido pelo OEM em uma cadeia de caracteres ANSI ou de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-200">Converte um número especificado de caracteres em uma cadeia de caractere do conjunto de caracteres definido pelo OEM em uma cadeia de caracteres ANSI ou de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ca8f-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-202">Grava dados formatados no buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ca8f-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ca8f-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="5ca8f-204">Grava dados formatados no buffer especificado usando um ponteiro para uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="5ca8f-205">Funções strsafe</span><span class="sxs-lookup"><span data-stu-id="5ca8f-205">Strsafe Functions</span></span>



| <span data-ttu-id="5ca8f-206">Nome</span><span class="sxs-lookup"><span data-stu-id="5ca8f-206">Name</span></span>                                             | <span data-ttu-id="5ca8f-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ca8f-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ca8f-208">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="5ca8f-209">Concatena uma cadeia de caracteres a outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="5ca8f-210">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="5ca8f-211">Concatena uma cadeia de caracteres a outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="5ca8f-212">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="5ca8f-213">Concatena o número especificado de bytes de uma cadeia de caracteres para outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="5ca8f-214">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="5ca8f-215">Concatena o número especificado de bytes de uma cadeia de caracteres para outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="5ca8f-216">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="5ca8f-217">Copia uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="5ca8f-218">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="5ca8f-219">Copia uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="5ca8f-220">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="5ca8f-221">Copia o número especificado de bytes de uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="5ca8f-222">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="5ca8f-223">Copia o número especificado de bytes de uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="5ca8f-224">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="5ca8f-225">Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="5ca8f-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="5ca8f-226">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="5ca8f-227">Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="5ca8f-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="5ca8f-228">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="5ca8f-229">Determina se uma cadeia de caracteres excede o comprimento especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="5ca8f-230">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="5ca8f-231">Grava dados formatados na cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="5ca8f-232">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="5ca8f-233">Grava dados formatados na cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="5ca8f-234">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="5ca8f-235">Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="5ca8f-236">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="5ca8f-237">Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="5ca8f-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="5ca8f-239">Concatena uma cadeia de caracteres a outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="5ca8f-240">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="5ca8f-241">Concatena uma cadeia de caracteres a outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="5ca8f-242">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="5ca8f-243">Concatena o número especificado de caracteres de uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="5ca8f-244">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="5ca8f-245">Concatena o número especificado de caracteres de uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="5ca8f-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="5ca8f-247">Copia uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="5ca8f-248">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="5ca8f-249">Copia uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="5ca8f-250">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="5ca8f-251">Copia o número especificado de caracteres de uma cadeia para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="5ca8f-252">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="5ca8f-253">Copia o número especificado de caracteres de uma cadeia para outra.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="5ca8f-254">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="5ca8f-255">Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="5ca8f-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="5ca8f-256">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="5ca8f-257">Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="5ca8f-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="5ca8f-258">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="5ca8f-259">Determina se uma cadeia de caracteres excede o comprimento especificado, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="5ca8f-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="5ca8f-261">Grava dados formatados na cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="5ca8f-262">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="5ca8f-263">Grava dados formatados na cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="5ca8f-264">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="5ca8f-265">Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="5ca8f-266">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="5ca8f-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="5ca8f-267">Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ca8f-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

