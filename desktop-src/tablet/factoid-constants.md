---
description: Define valores de cadeia de caracteres constantes que são usados para aumentar a precisão do reconhecimento fornecendo informações contextuais para o reconhecedor.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes do factor (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501836"
---
# <a name="factoid-constants"></a><span data-ttu-id="749fd-103">Constantes do factor</span><span class="sxs-lookup"><span data-stu-id="749fd-103">Factoid Constants</span></span>

<span data-ttu-id="749fd-104">Define valores de cadeia de caracteres constantes que são usados para aumentar a precisão do reconhecimento fornecendo informações contextuais para o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="749fd-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="749fd-105">Nome</span><span class="sxs-lookup"><span data-stu-id="749fd-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="749fd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="749fd-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="749fd-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-108">Desabilita todas as outras paradeleções e dicionários.</span><span class="sxs-lookup"><span data-stu-id="749fd-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="749fd-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-110">A configuração padrão de factores para idiomas ocidentais inclui o dicionário do sistema, o dicionário do usuário, várias pontuações e o factor da Web e do número.</span><span class="sxs-lookup"><span data-stu-id="749fd-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="749fd-111">A configuração padrão para o factos para idiomas do leste asiático inclui todos os caracteres suportados pelo reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="749fd-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="749fd-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-113">Indica para um reconhecedor usar apenas o dicionário do sistema.</span><span class="sxs-lookup"><span data-stu-id="749fd-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="749fd-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-115">Indica para um reconhecedor usar uma lista de palavras definida de forma programática.</span><span class="sxs-lookup"><span data-stu-id="749fd-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="749fd-116">A lista de palavras é definida <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>pela propriedade</strong></a> KeyList de um objeto <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="749fd-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-117">Se uma cadeia de caracteres for adicionada a uma lista de palavras, suas versões em maiúsculas também serão adicionadas implicitamente.</span><span class="sxs-lookup"><span data-stu-id="749fd-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="749fd-118">Por exemplo, adicionar &quot; Hello &quot; implicitamente adiciona &quot; Hello &quot; e &quot; Hello &quot; .</span><span class="sxs-lookup"><span data-stu-id="749fd-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="749fd-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-120">Indica para um reconhecedor procurar um endereço de email.</span><span class="sxs-lookup"><span data-stu-id="749fd-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-121">Um endereço de email totalmente qualificado, como &quot; someone@example.com &quot; , deve ser usado para esse factor.</span><span class="sxs-lookup"><span data-stu-id="749fd-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="749fd-122">Um alias solitário, como &quot; alguém &quot; , não é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="749fd-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="749fd-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-124">Indica para um reconhecedor procurar um endereço da Web.</span><span class="sxs-lookup"><span data-stu-id="749fd-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="749fd-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-126">Indica para um reconhecedor procurar um único caractere.</span><span class="sxs-lookup"><span data-stu-id="749fd-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-127">Esse factor procura por qualquer caractere ANSI isolado.</span><span class="sxs-lookup"><span data-stu-id="749fd-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="749fd-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-129">Indica para um reconhecedor procurar um número.</span><span class="sxs-lookup"><span data-stu-id="749fd-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-130">Os valores numéricos incluem separadores, decimais, ordinais e outros símbolos numéricos comumente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="749fd-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-132">Indica para um reconhecedor procurar um único dígito, de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="749fd-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="749fd-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-134">Fornece um contexto numérico simples para um reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="749fd-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-135">Esse factor não tem suporte nesta versão do SDK do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="749fd-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="749fd-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-137">Indica para um reconhecedor procurar caracteres que denotam um valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="749fd-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="749fd-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-139">Indica para um reconhecedor procurar CEPs.</span><span class="sxs-lookup"><span data-stu-id="749fd-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="749fd-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-141">Indica para um reconhecedor procurar por porcentagens.</span><span class="sxs-lookup"><span data-stu-id="749fd-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="749fd-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-143">Indica para um reconhecedor procurar caracteres que denotam uma data.</span><span class="sxs-lookup"><span data-stu-id="749fd-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="749fd-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-145">Indica para um reconhecedor procurar caracteres que denotam uma hora.</span><span class="sxs-lookup"><span data-stu-id="749fd-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="749fd-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-147">Indica para um reconhecedor procurar caracteres que denotam um número de telefone.</span><span class="sxs-lookup"><span data-stu-id="749fd-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="749fd-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-149">Indica para um reconhecedor procurar caracteres que denotam um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="749fd-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="749fd-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-151">Indica para um reconhecedor procurar um caractere maiúsculo único: A a Z.</span><span class="sxs-lookup"><span data-stu-id="749fd-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="749fd-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-153">Indica para um reconhecedor procurar um caractere minúsculo em minúsculas: A a Z.</span><span class="sxs-lookup"><span data-stu-id="749fd-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-154">Esse factor não tem suporte nesta versão do SDK do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="749fd-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="749fd-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-156">Indica para um reconhecedor procurar caracteres de pontuação.</span><span class="sxs-lookup"><span data-stu-id="749fd-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-157">Esse factor não tem suporte nesta versão do SDK do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="749fd-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="749fd-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-159">Indica para um reconhecedor procurar caracteres kanji, Katakana e hiragana usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="749fd-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="749fd-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-161">Indica para um reconhecedor procurar caracteres chineses simplificados comumente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="749fd-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-163">Indica para um reconhecedor procurar caracteres chineses tradicionais usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="749fd-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="749fd-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-165">Indica para um reconhecedor procurar caracteres coreanos comumente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="749fd-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-167">Indica para um reconhecedor procurar somente caracteres hiragana.</span><span class="sxs-lookup"><span data-stu-id="749fd-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="749fd-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-169">Indica para um reconhecedor procurar somente caracteres Katakana.</span><span class="sxs-lookup"><span data-stu-id="749fd-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="749fd-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-171">Indica para um reconhecedor procurar caracteres kanji comumente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="749fd-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-173">Indica para um reconhecedor procurar caracteres kanji raramente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-174">Esse factor não tem suporte nesta versão do SDK do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="749fd-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="749fd-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-176">Indica para um reconhecedor procurar caracteres bopomofo.</span><span class="sxs-lookup"><span data-stu-id="749fd-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="749fd-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-178">Indica para um reconhecedor procurar caracteres Hangul de compatibilidade com a Jamo.</span><span class="sxs-lookup"><span data-stu-id="749fd-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="749fd-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-180">Indica para um reconhecedor procurar caracteres Hangul usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="749fd-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="749fd-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="749fd-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="749fd-182">Indica para um reconhecedor procurar caracteres Hangul raramente usados.</span><span class="sxs-lookup"><span data-stu-id="749fd-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="749fd-183">Esse factor não tem suporte nesta versão do SDK do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="749fd-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="749fd-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="749fd-184">Remarks</span></span>

<span data-ttu-id="749fd-185">Em C++, você pode acessar essas constantes no arquivo de cabeçalho Msinkaut. h, que está localizado no <systemdrive> diretório: \\ arquivos \\ de programas Microsoft Tablet PC Platform SDK \\ include se você instalou o SDK no local padrão.</span><span class="sxs-lookup"><span data-stu-id="749fd-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="749fd-186">Essas constantes são WCHARs, não BSTRs.</span><span class="sxs-lookup"><span data-stu-id="749fd-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="749fd-187">Eles devem ser convertidos em BSTRs antes de usar como parâmetros para métodos de objeto.</span><span class="sxs-lookup"><span data-stu-id="749fd-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="749fd-188">Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="749fd-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="749fd-189">Para os reconhecedores do script Latin, as factos definidas nessa classe são fornecidas apenas para fins de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="749fd-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="749fd-190">Para o novo desenvolvimento, você é incentivado a usar os valores definidos na função [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) .</span><span class="sxs-lookup"><span data-stu-id="749fd-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="749fd-191">Para obter detalhes, consulte [usando o contexto para melhorar a precisão](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="749fd-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="749fd-192">Use esses identificadores para especificar qual factor deve ser usado durante o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="749fd-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="749fd-193">As seguintes combinações de factors têm suporte apenas para idiomas ocidentais.</span><span class="sxs-lookup"><span data-stu-id="749fd-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="749fd-194">Elas não têm definições separadas, mas são entradas literais de cadeia de caracteres aceitáveis para a propriedade [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de objetos que usam os factos.</span><span class="sxs-lookup"><span data-stu-id="749fd-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="749fd-195">Essas constantes de cadeia de caracteres de facto permitem que a entrada corresponda a qualquer um dos factos na expressão.</span><span class="sxs-lookup"><span data-stu-id="749fd-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="749fd-196">Combinação</span><span class="sxs-lookup"><span data-stu-id="749fd-196">Combination</span></span>               | <span data-ttu-id="749fd-197">Definição</span><span class="sxs-lookup"><span data-stu-id="749fd-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="749fd-198">"listas de palavras da WEB \| "</span><span class="sxs-lookup"><span data-stu-id="749fd-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="749fd-199">O facto da Web ou a lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="749fd-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="749fd-200">"listas de palavras de EMAIL \| "</span><span class="sxs-lookup"><span data-stu-id="749fd-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="749fd-201">O facto de email ou a lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="749fd-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="749fd-202">" \| listas de palavras da Web de nome de arquivo \| "</span><span class="sxs-lookup"><span data-stu-id="749fd-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="749fd-203">O nome do arquivo ou o factor da Web ou a lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="749fd-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="749fd-204">Se você estiver usando o controle [InkEdit](inkedit-control-reference.md) , o factor poderá ser definido como uma propriedade do controle.</span><span class="sxs-lookup"><span data-stu-id="749fd-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="749fd-205">Se você estiver usando as APIs de plataforma do Tablet PC, poderá definir a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) em um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="749fd-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="749fd-206">Como alternativa, você pode definir essa propriedade com a constante de cadeia de caracteres de factor real.</span><span class="sxs-lookup"><span data-stu-id="749fd-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="749fd-207">Constantes de cadeia de caracteres de facto diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="749fd-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="749fd-208">Para obter mais informações sobre os factos e como usá-los, consulte usando o contexto para [melhorar a precisão](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="749fd-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="749fd-209">Para determinar se um factor está disponível em um idioma específico, consulte as [edições com suporte na versão 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="749fd-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="749fd-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="749fd-210">Requirements</span></span>



| <span data-ttu-id="749fd-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="749fd-211">Requirement</span></span> | <span data-ttu-id="749fd-212">Valor</span><span class="sxs-lookup"><span data-stu-id="749fd-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="749fd-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="749fd-213">Minimum supported client</span></span><br/> | <span data-ttu-id="749fd-214">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="749fd-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="749fd-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="749fd-215">Minimum supported server</span></span><br/> | <span data-ttu-id="749fd-216">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="749fd-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="749fd-217">parâmetro</span><span class="sxs-lookup"><span data-stu-id="749fd-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="749fd-218"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="749fd-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="749fd-219">Confira também</span><span class="sxs-lookup"><span data-stu-id="749fd-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="749fd-220">[**Classe InkRecognizeContext de Propriedade do factor \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="749fd-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="749fd-221">[**Classe PenInputPanel de Propriedade do factor \[\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="749fd-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="749fd-222">[**Controle de Propriedade InkEdit do factor \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="749fd-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="749fd-223">Usando o contexto para melhorar a precisão</span><span class="sxs-lookup"><span data-stu-id="749fd-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="749fd-224">Factos com suporte da versão 1</span><span class="sxs-lookup"><span data-stu-id="749fd-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

