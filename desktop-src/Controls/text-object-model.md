---
title: Modelo de objeto de texto
description: Esta seção contém informações sobre os elementos de programação usados com o modelo de objeto de texto (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824037"
---
# <a name="text-object-model"></a><span data-ttu-id="c546f-103">Modelo de objeto de texto</span><span class="sxs-lookup"><span data-stu-id="c546f-103">Text Object Model</span></span>

<span data-ttu-id="c546f-104">Esta seção contém informações sobre os elementos de programação usados com o modelo de objeto de texto (TOM).</span><span class="sxs-lookup"><span data-stu-id="c546f-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="c546f-105">José define um conjunto substancial de interfaces de manipulação de texto.</span><span class="sxs-lookup"><span data-stu-id="c546f-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="c546f-106">Soluções de texto como o Microsoft Word e os controles rich edit dão suporte ao conjunto de recursos TOM.</span><span class="sxs-lookup"><span data-stu-id="c546f-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="c546f-107">José foi bastante influenciado pelo WordBasic (a linguagem de programação usada para o Word) e é fácil de usar do Microsoft Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="c546f-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="c546f-108">Essa compatibilidade tem várias vantagens:</span><span class="sxs-lookup"><span data-stu-id="c546f-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="c546f-109">O código pode migrar razoavelmente facilmente de uma solução para outra.</span><span class="sxs-lookup"><span data-stu-id="c546f-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="c546f-110">Uma linguagem pode ser usada para compartilhar informações de texto entre diferentes mecanismos de texto.</span><span class="sxs-lookup"><span data-stu-id="c546f-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="c546f-111">Ele reduz a necessidade de documentação e código em comparação com as interfaces COM (Component Object Model de baixo nível) e VBA separadas.</span><span class="sxs-lookup"><span data-stu-id="c546f-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="c546f-112">No entanto, isso pode ser menos eficiente para fins de C/C++ do que o uso de interfaces COM de nível inferior mais gerais.</span><span class="sxs-lookup"><span data-stu-id="c546f-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="c546f-113">José é um conjunto simples de interfaces a serem implementadas para suas soluções de texto primários, palavras e controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="c546f-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="c546f-114">No entanto, para aplicativos que colocam ênfase mínima no texto, é melhor fornecer interfaces de TOM transferindo o texto para um controle de edição que dá suporte a TOM.</span><span class="sxs-lookup"><span data-stu-id="c546f-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="c546f-115">Como os controles de edição avançados são fornecidos com os sistemas operacionais da Microsoft, eles são o meio padrão de obter a funcionalidade de TOM.</span><span class="sxs-lookup"><span data-stu-id="c546f-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="c546f-116">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="c546f-116">Overviews</span></span>



| <span data-ttu-id="c546f-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="c546f-117">Topic</span></span>                                                          | <span data-ttu-id="c546f-118">Sumário</span><span class="sxs-lookup"><span data-stu-id="c546f-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c546f-119">Sobre o modelo de objeto de texto</span><span class="sxs-lookup"><span data-stu-id="c546f-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="c546f-120">O objeto TOM (modelo de objeto de texto) de nível superior é definido pela interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , que tem métodos para criar e recuperar objetos inferiores na hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="c546f-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="c546f-121">Usando o modelo de objeto de texto</span><span class="sxs-lookup"><span data-stu-id="c546f-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="c546f-122">Os exemplos de código neste documento mostram vários aspectos do uso do TOM (modelo de objeto de texto).</span><span class="sxs-lookup"><span data-stu-id="c546f-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="c546f-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c546f-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c546f-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="c546f-124">Topic</span></span></th>
<th><span data-ttu-id="c546f-125">Sumário</span><span class="sxs-lookup"><span data-stu-id="c546f-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c546f-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="c546f-127">A interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> é a interface de alto nível de Tom, que recupera a seleção ativa e os objetos de intervalo para qualquer história no documento, esteja ela ativa ou não.</span><span class="sxs-lookup"><span data-stu-id="c546f-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="c546f-128">Ele permite que o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c546f-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="c546f-129">Abra e salve documentos.</span><span class="sxs-lookup"><span data-stu-id="c546f-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="c546f-130">Controlar o comportamento de desfazer e a atualização de tela.</span><span class="sxs-lookup"><span data-stu-id="c546f-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="c546f-131">Localize um intervalo de uma posição de tela.</span><span class="sxs-lookup"><span data-stu-id="c546f-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="c546f-132">Obtenha um enumerador de história do <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c546f-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="c546f-133"><strong>Quando implementar</strong></span><span class="sxs-lookup"><span data-stu-id="c546f-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="c546f-134">Normalmente, os aplicativos não implementam a interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c546f-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="c546f-135">Soluções de texto da Microsoft, como controles de edição avançados, implementam <strong>ITextDocument</strong> como parte de sua implementação de Tom.</span><span class="sxs-lookup"><span data-stu-id="c546f-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="c546f-136"><strong>Quando usar</strong></span><span class="sxs-lookup"><span data-stu-id="c546f-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="c546f-137">Os aplicativos podem recuperar um ponteiro <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c546f-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="c546f-138">Para fazer isso, envie uma mensagem de <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> para recuperar um objeto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c546f-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="c546f-139">Em seguida, chame o método <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> do objeto para recuperar um ponteiro <strong>ITextDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="c546f-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c546f-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="c546f-141">José os atributos de intervalo de texto avançados são acessados por meio de um par de interfaces duplas, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c546f-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c546f-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="c546f-143">José os atributos de intervalo de texto avançados são acessados por meio de um par de interfaces duplas, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c546f-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c546f-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="c546f-145">Os objetos <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> são ferramentas poderosas de edição e vinculação de dados que permitem que um programa selecione texto em uma história e, em seguida, examine ou altere esse texto.</span><span class="sxs-lookup"><span data-stu-id="c546f-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c546f-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="c546f-147">Uma seleção de texto é um intervalo de texto com realce de seleção.</span><span class="sxs-lookup"><span data-stu-id="c546f-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c546f-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="c546f-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="c546f-149">A finalidade da interface <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> é enumerar as histórias em um <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c546f-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

