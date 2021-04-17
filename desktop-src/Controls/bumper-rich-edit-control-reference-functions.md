---
title: Funções de edição avançadas
description: Funções de edição avançadas
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105748721"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="659cc-103">Funções de edição avançadas</span><span class="sxs-lookup"><span data-stu-id="659cc-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="659cc-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="659cc-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="659cc-105">Tópico</span><span class="sxs-lookup"><span data-stu-id="659cc-105">Topic</span></span></th>
<th><span data-ttu-id="659cc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="659cc-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="659cc-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span><span class="sxs-lookup"><span data-stu-id="659cc-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="659cc-108">A função <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> é uma função de retorno de chamada definida pelo aplicativo que é usada com a mensagem de <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="659cc-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659cc-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="659cc-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="659cc-110">A função <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com as mensagens de <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> e <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="659cc-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="659cc-111">Ele é usado para transferir um fluxo de dados para dentro ou para fora de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="659cc-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="659cc-112">O tipo <strong>EditStreamCallback</strong> define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="659cc-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="659cc-113"><em>EditStreamCallback</em> é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="659cc-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="659cc-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span><span class="sxs-lookup"><span data-stu-id="659cc-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="659cc-115">A função <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a mensagem de <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="659cc-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="659cc-116">Ele determina o índice de caracteres da quebra de palavra ou a classe de caractere e os sinalizadores de quebra de palavras dos caracteres no texto especificado.</span><span class="sxs-lookup"><span data-stu-id="659cc-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="659cc-117">O tipo <strong>EDITWORDBREAKPROCEX</strong> define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="659cc-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="659cc-118"><em>EditWordBreakProcEx</em> é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="659cc-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659cc-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-120">Recupera o formato UTF (Unicode Transformation Format)-32 matemático alfanuméricos que corresponde ao caractere básico de plano multilíngüe (BMP) e ao estilo matemático.</span><span class="sxs-lookup"><span data-stu-id="659cc-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="659cc-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-122">Recupera o estilo matemático e o código de caractere básico de plano multilíngue (BMP) que corresponde ao byte à direita especificado de um par de substitutos de matemática.</span><span class="sxs-lookup"><span data-stu-id="659cc-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659cc-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span><span class="sxs-lookup"><span data-stu-id="659cc-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="659cc-124">A função <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a mensagem de <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="659cc-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="659cc-125">Ele determina como a hifenização é feita em um controle de edição rico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="659cc-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="659cc-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-127">Traduz os objetos internos de matemática, Ruby e outros incorporados no intervalo especificado para o formulário linear.</span><span class="sxs-lookup"><span data-stu-id="659cc-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659cc-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-129">Converte a matemática de formato linear em um intervalo em um formulário interno ou modifica o formulário atual criado.</span><span class="sxs-lookup"><span data-stu-id="659cc-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="659cc-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-131">Traduz os caracteres matemáticos no intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="659cc-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="659cc-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span><span class="sxs-lookup"><span data-stu-id="659cc-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="659cc-133">Registra dois nomes de classe, REListBox20W e RECombobox20W, que podem ser usados para criar janelas de caixa de listagem de edição rica ou de caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="659cc-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="659cc-134">Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="659cc-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="659cc-135">Essa função pode não ter suporte em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="659cc-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

