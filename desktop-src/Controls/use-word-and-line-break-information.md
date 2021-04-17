---
title: Como usar o Word e as informações de quebra de linha
description: Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105754800"
---
# <a name="how-to-use-word-and-line-break-information"></a><span data-ttu-id="6b037-103">Como usar o Word e as informações de quebra de linha</span><span class="sxs-lookup"><span data-stu-id="6b037-103">How to Use Word and Line Break Information</span></span>

<span data-ttu-id="6b037-104">Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas.</span><span class="sxs-lookup"><span data-stu-id="6b037-104">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="6b037-105">O controle usa essas informações ao executar operações de quebra automática de texto e ao processar CTRL + tecla de seta para a esquerda e CTRL + seta para a direita combinações de teclas.</span><span class="sxs-lookup"><span data-stu-id="6b037-105">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="6b037-106">Um aplicativo pode enviar mensagens para um controle de edição rico para substituir o procedimento de quebra de palavra padrão, para recuperar informações de quebra de palavra e para determinar em qual linha um determinado caractere se encontra.</span><span class="sxs-lookup"><span data-stu-id="6b037-106">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6b037-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="6b037-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6b037-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="6b037-108">Technologies</span></span>

-   [<span data-ttu-id="6b037-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="6b037-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6b037-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6b037-110">Prerequisites</span></span>

-   <span data-ttu-id="6b037-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6b037-111">C/C++</span></span>
-   <span data-ttu-id="6b037-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="6b037-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6b037-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="6b037-113">Instructions</span></span>

### <a name="use-word-and-line-break-information"></a><span data-ttu-id="6b037-114">Usar informações de quebra de linha e de palavras</span><span class="sxs-lookup"><span data-stu-id="6b037-114">Use Word and Line Break Information</span></span>

<span data-ttu-id="6b037-115">Os procedimentos de quebra de palavras para controles de edição avançados são semelhantes aos de controles de edição, mas têm recursos adicionais: os procedimentos de quebra de palavras para ambos os tipos de controles podem determinar se um caractere é um delimitador e encontrar a quebra de palavra mais próxima antes ou depois da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="6b037-115">Word-break procedures for rich edit controls are similar to those for edit controls, but they have additional capabilities: word-break procedures for both kinds of controls can determine whether a character is a delimiter and can find the nearest word break before or after the specified position.</span></span> <span data-ttu-id="6b037-116">Um delimitador é um caractere que marca o final de uma palavra, como um espaço.</span><span class="sxs-lookup"><span data-stu-id="6b037-116">A delimiter is a character that marks the end of a word, such as a space.</span></span> <span data-ttu-id="6b037-117">Normalmente, em um controle de edição, uma quebra de palavra ocorre somente após os delimitadores.</span><span class="sxs-lookup"><span data-stu-id="6b037-117">Usually, in an edit control, a word break occurs only after delimiters.</span></span> <span data-ttu-id="6b037-118">No entanto, regras diferentes se aplicam à maioria dos idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="6b037-118">However, different rules apply to most Asian languages.</span></span>

<span data-ttu-id="6b037-119">Os procedimentos de quebra de palavras para controles de edição avançados também agrupam caracteres em classes de caracteres, cada um identificado por um valor no intervalo de 0x00 a 0x0F.</span><span class="sxs-lookup"><span data-stu-id="6b037-119">Word-break procedures for rich edit controls also group characters into character classes, each identified by a value in the range 0x00 through 0x0F.</span></span> <span data-ttu-id="6b037-120">As quebras ocorrem após delimitadores ou entre caracteres de classes diferentes.</span><span class="sxs-lookup"><span data-stu-id="6b037-120">Breaks occur either after delimiters or between characters of different classes.</span></span> <span data-ttu-id="6b037-121">Assim, um procedimento de quebra de palavra com classes diferentes para caracteres alfanuméricos e de Pontuação encontraria duas quebras de palavra na cadeia de caracteres "Win.doc" (antes e depois do período).</span><span class="sxs-lookup"><span data-stu-id="6b037-121">Thus, a word-break procedure with different classes for alphanumeric and punctuation characters would find two word breaks in the string "Win.doc" (before and after the period).</span></span>

<span data-ttu-id="6b037-122">A classe de um caractere pode ser combinada com zero ou mais sinalizadores de quebra de palavras para formar um valor de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6b037-122">A character's class can be combined with zero or more word-break flags to form an 8-bit value.</span></span> <span data-ttu-id="6b037-123">Ao executar operações de quebra automática de linha, um controle de edição rico usa sinalizadores de quebra de palavras para determinar onde ele pode quebrar linhas.</span><span class="sxs-lookup"><span data-stu-id="6b037-123">When performing word-wrap operations, a rich edit control uses word-break flags to determine where it can break lines.</span></span> <span data-ttu-id="6b037-124">A edição avançada usa os seguintes sinalizadores de quebra de palavra.</span><span class="sxs-lookup"><span data-stu-id="6b037-124">Rich Edit uses the following word-break flags.</span></span>



| <span data-ttu-id="6b037-125">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="6b037-125">Flag</span></span>            | <span data-ttu-id="6b037-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b037-126">Description</span></span>                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b037-127">WBF \_ BREAKAFTER</span><span class="sxs-lookup"><span data-stu-id="6b037-127">WBF\_BREAKAFTER</span></span> | <span data-ttu-id="6b037-128">As linhas podem ser quebradas após o caractere.</span><span class="sxs-lookup"><span data-stu-id="6b037-128">Lines may be broken after the character.</span></span>                                                                                          |
| <span data-ttu-id="6b037-129">\_divisão WBF</span><span class="sxs-lookup"><span data-stu-id="6b037-129">WBF\_BREAKLINE</span></span>  | <span data-ttu-id="6b037-130">O caractere é um delimitador.</span><span class="sxs-lookup"><span data-stu-id="6b037-130">The character is a delimiter.</span></span> <span data-ttu-id="6b037-131">Os delimitadores marcam as extremidades das palavras.</span><span class="sxs-lookup"><span data-stu-id="6b037-131">Delimiters mark the ends of words.</span></span> <span data-ttu-id="6b037-132">As linhas podem ser quebradas após os delimitadores.</span><span class="sxs-lookup"><span data-stu-id="6b037-132">Lines may be broken after delimiters.</span></span>                            |
| <span data-ttu-id="6b037-133">WBF \_ ISwhite</span><span class="sxs-lookup"><span data-stu-id="6b037-133">WBF\_ISWHITE</span></span>    | <span data-ttu-id="6b037-134">O caractere é um caractere de espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="6b037-134">The character is a white-space character.</span></span> <span data-ttu-id="6b037-135">Os caracteres de espaço em branco à direita não são incluídos no comprimento de uma linha durante o encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="6b037-135">Trailing white-space characters are not included in the length of a line when wrapping.</span></span> |



 

<span data-ttu-id="6b037-136">O \_ valor de BREAKAFTER WBF é usado para permitir o encapsulamento após um caractere que não marca o fim de uma palavra, como um hífen.</span><span class="sxs-lookup"><span data-stu-id="6b037-136">The WBF\_BREAKAFTER value is used to allow wrapping after a character that does not mark the end of a word, such as a hyphen.</span></span>

<span data-ttu-id="6b037-137">Você pode substituir o procedimento de quebra de palavra padrão por um controle de edição rico por seu próprio procedimento usando a mensagem em [**\_ SETWORDBREAKPROC**](em-setwordbreakproc.md) .</span><span class="sxs-lookup"><span data-stu-id="6b037-137">You can replace the default word-break procedure for a rich edit control with your own procedure by using the [**EM\_SETWORDBREAKPROC**](em-setwordbreakproc.md) message.</span></span> <span data-ttu-id="6b037-138">Para obter mais informações sobre os procedimentos de quebra de palavras, consulte a descrição da função [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="6b037-138">For more information about word-break procedures, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="6b037-139">Essa substituição não é recomendada para o Microsoft rich edit 2,0 e posterior, devido à complexidade da separação de palavras multilíngues.</span><span class="sxs-lookup"><span data-stu-id="6b037-139">This replacement is not recommended for Microsoft Rich Edit 2.0 and later, due to the complexity of multilingual word breaking.</span></span>

 

<span data-ttu-id="6b037-140">Para o Microsoft Rich Edit 1,0, você pode usar a mensagem em [**\_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) para substituir o procedimento de quebra de palavra estendido padrão por uma função [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) .</span><span class="sxs-lookup"><span data-stu-id="6b037-140">For Microsoft Rich Edit 1.0, you can use the [**EM\_SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) message to replace the default extended word-break procedure with an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function.</span></span> <span data-ttu-id="6b037-141">Essa função fornece informações adicionais sobre o texto, como o conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b037-141">This function provides additional information about the text, such as the character set.</span></span> <span data-ttu-id="6b037-142">Você pode usar a mensagem em [**\_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) para recuperar o endereço do procedimento de quebra de palavra estendido atual.</span><span class="sxs-lookup"><span data-stu-id="6b037-142">You can use the [**EM\_GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) message to retrieve the address of the current extended word-break procedure.</span></span> <span data-ttu-id="6b037-143">Observe que o Microsoft rich edit 2,0 e posterior não dão suporte a *EditWordBreakProcEx*, em **\_ GETWORDBREAKPROCEX** e em **\_ SETWORDBREAKPROCEX**.</span><span class="sxs-lookup"><span data-stu-id="6b037-143">Note that Microsoft Rich Edit 2.0 and later do not support *EditWordBreakProcEx*, **EM\_GETWORDBREAKPROCEX**, and **EM\_SETWORDBREAKPROCEX**.</span></span>

<span data-ttu-id="6b037-144">Você pode usar a mensagem em [**\_ FINDWORDBREAK**](em-findwordbreak.md) para localizar quebras de palavras ou para determinar a classe de um caractere e os sinalizadores de quebra de palavras.</span><span class="sxs-lookup"><span data-stu-id="6b037-144">You can use the [**EM\_FINDWORDBREAK**](em-findwordbreak.md) message to find word breaks or to determine a character's class and word-break flags.</span></span> <span data-ttu-id="6b037-145">Por sua vez, o controle chama seu procedimento de quebra de palavra para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="6b037-145">In turn, the control calls its word-break procedure to get the requested information.</span></span>

<span data-ttu-id="6b037-146">Para determinar em qual linha um determinado caractere se encontra, você pode usar a mensagem em [**\_ EXLINEFROMCHAR**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="6b037-146">To determine which line a given character falls on, you can use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b037-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b037-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b037-148">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="6b037-148">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="6b037-149">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="6b037-149">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 