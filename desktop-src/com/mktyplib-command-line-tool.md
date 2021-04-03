---
title: Ferramenta de Command-Line de MkTypLib
description: MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos. Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641934"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="1d2e5-104">Ferramenta de Command-Line de MkTypLib</span><span class="sxs-lookup"><span data-stu-id="1d2e5-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="1d2e5-105">\[A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="1d2e5-106">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="1d2e5-107">Se precisar de compatibilidade com versões anteriores com programas de automação antigos, use o compilador MIDL com a opção **/mktyplib203** .\]</span><span class="sxs-lookup"><span data-stu-id="1d2e5-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="1d2e5-108">MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="1d2e5-109">Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="1d2e5-110">Para gerar uma biblioteca de tipos a partir de um arquivo ODL:</span><span class="sxs-lookup"><span data-stu-id="1d2e5-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="1d2e5-111">No prompt de comando, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="1d2e5-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="1d2e5-112">\**mktyplibÂ \* \* \* nome de arquivo*</span><span class="sxs-lookup"><span data-stu-id="1d2e5-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="1d2e5-113">em que *filename* é o nome do arquivo ODL.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="1d2e5-114">O MkTypLib também dá suporte a vários parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="1d2e5-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="1d2e5-115">Para obter uma lista completa, execute a seguinte linha de comando:</span><span class="sxs-lookup"><span data-stu-id="1d2e5-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="1d2e5-116">**MkTypLib/?**</span><span class="sxs-lookup"><span data-stu-id="1d2e5-116">**mktyplib /?**</span></span>

<span data-ttu-id="1d2e5-117">Como MkTypLib é um aplicativo obsoleto, ele não pode analisar arquivos IDL ou arquivos com interfaces definidas fora de uma instrução de [**biblioteca**](/windows/desktop/Midl/library) .</span><span class="sxs-lookup"><span data-stu-id="1d2e5-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="1d2e5-118">Para obter mais informações, consulte [diferenças entre MIDL e MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="1d2e5-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d2e5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d2e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d2e5-120">Convertendo para C++</span><span class="sxs-lookup"><span data-stu-id="1d2e5-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 