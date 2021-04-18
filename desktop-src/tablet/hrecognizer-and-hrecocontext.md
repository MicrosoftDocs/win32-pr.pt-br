---
description: Você faz referência a um reconhecedor de tinta com um identificador HRECOGNIZER e um contexto de reconhecedor como um identificador HRECOCONTEXT. Uma DLL (biblioteca de vínculo dinâmico) do reconhecedor pode implementar reconhecedores para mais de um idioma.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER e HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787698"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="41173-103">HRECOGNIZER e HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="41173-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="41173-104">Você faz referência a um reconhecedor de tinta com um identificador [HRECOGNIZER](hrecognizer-handle.md) e um contexto de reconhecedor como um identificador [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="41173-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="41173-105">Uma DLL (biblioteca de vínculo dinâmico) do reconhecedor pode implementar reconhecedores para mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="41173-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="41173-106">Nesse caso, cada idioma é selecionado por um CLSID que é passado ao criar o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="41173-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="41173-107">Além disso, uma DLL de reconhecimento pode criar vários identificadores de reconhecedor quando ele é carregado, um ou mais para cada idioma reconhecido.</span><span class="sxs-lookup"><span data-stu-id="41173-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="41173-108">Um contexto de reconhecedor é criado para representar o evento de reconhecimento de uma folha de tinta específica.</span><span class="sxs-lookup"><span data-stu-id="41173-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="41173-109">Quando o contexto é criado, o identificador de objetos do reconhecedor associado é passado para a função [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .</span><span class="sxs-lookup"><span data-stu-id="41173-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="41173-110">Isso associa o idioma ao contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="41173-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="41173-111">Um contexto de reconhecedor pode representar o reconhecimento de toda a tinta no corpo de um email, a tinta de um único campo dentro de um aplicativo ou uma única linha de texto gravada no painel de entrada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="41173-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="41173-112">O volume de tinta em um único contexto de reconhecedor pode variar de um único traço para uma página inteira ou mais.</span><span class="sxs-lookup"><span data-stu-id="41173-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="41173-113">O contexto do reconhecedor é definido pelas configurações de:</span><span class="sxs-lookup"><span data-stu-id="41173-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="41173-114">O guia de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="41173-114">The recognition guide.</span></span>
-   <span data-ttu-id="41173-115">Quaisquer factos.</span><span class="sxs-lookup"><span data-stu-id="41173-115">Any factoids.</span></span>
-   <span data-ttu-id="41173-116">Quaisquer sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="41173-116">Any flags.</span></span>
-   <span data-ttu-id="41173-117">O contexto do texto.</span><span class="sxs-lookup"><span data-stu-id="41173-117">The text context.</span></span>
-   <span data-ttu-id="41173-118">Qualquer lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="41173-118">Any word list.</span></span>
-   <span data-ttu-id="41173-119">O modo de preenchimento automático de caractere.</span><span class="sxs-lookup"><span data-stu-id="41173-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="41173-120">O identificador do contexto do reconhecedor é passado para todas as funções que usam essas configurações.</span><span class="sxs-lookup"><span data-stu-id="41173-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="41173-121">Alterar uma configuração altera o contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="41173-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="41173-122">O aplicativo pode usar vários contextos para reconhecer tinta de diferentes partes da tela.</span><span class="sxs-lookup"><span data-stu-id="41173-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="41173-123">Um contexto individual pode reconhecer várias linhas de texto.</span><span class="sxs-lookup"><span data-stu-id="41173-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="41173-124">No entanto, um contexto individual não pode processar dois parágrafos gravados lado a lado, como várias colunas em um artigo de jornal.</span><span class="sxs-lookup"><span data-stu-id="41173-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="41173-125">Para reconhecer a nova tinta, crie um novo contexto.</span><span class="sxs-lookup"><span data-stu-id="41173-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="41173-126">Como alternativa, use a função [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) para fazer uma cópia de um contexto que não tem a tinta e os resultados, ou a função [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) para limpar um contexto de sua tinta e dos resultados.</span><span class="sxs-lookup"><span data-stu-id="41173-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="41173-127">Com essas abordagens, um aplicativo de tinta pode reutilizar um contexto.</span><span class="sxs-lookup"><span data-stu-id="41173-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41173-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41173-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41173-129">**Função setguide**</span><span class="sxs-lookup"><span data-stu-id="41173-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="41173-130">**Função getguide**</span><span class="sxs-lookup"><span data-stu-id="41173-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="41173-131">**Função setfactoid**</span><span class="sxs-lookup"><span data-stu-id="41173-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="41173-132">**Função SetFlags**</span><span class="sxs-lookup"><span data-stu-id="41173-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="41173-133">**Função SetEnabledUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="41173-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="41173-134">**Função GetEnabledUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="41173-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="41173-135">**Função SetCACMode**</span><span class="sxs-lookup"><span data-stu-id="41173-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="41173-136">**Função SetTextContext**</span><span class="sxs-lookup"><span data-stu-id="41173-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="41173-137">**Função setwordlist**</span><span class="sxs-lookup"><span data-stu-id="41173-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



