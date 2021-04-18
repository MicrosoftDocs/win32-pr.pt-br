---
title: Gerando uma biblioteca de tipos com MIDL
description: O elemento de nível superior da sintaxe ODL é a instrução de biblioteca (bloco de biblioteca).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas, gerando uma biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752061"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="f33d3-104">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="f33d3-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="f33d3-105">O elemento de nível superior da sintaxe ODL é a instrução de biblioteca (bloco de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="f33d3-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="f33d3-106">Todas as outras instruções ODL, com exceção dos atributos aplicados à instrução da biblioteca, devem ser definidas dentro do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f33d3-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="f33d3-107">Quando o compilador MIDL vê um bloco de biblioteca, ele gera uma biblioteca de tipos praticamente da mesma forma que o MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="f33d3-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="f33d3-108">Com algumas exceções, descritas em [diferenças entre MIDL e MkTypLib](differences-between-midl-and-mktyplib.md), as instruções dentro do bloco de biblioteca devem seguir a mesma sintaxe do idioma ODL e MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="f33d3-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="f33d3-109">A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="f33d3-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="f33d3-110">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="f33d3-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="f33d3-111">Você pode aplicar atributos ODL a elementos que são definidos dentro ou fora do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f33d3-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="f33d3-112">Esses atributos não têm efeito fora do bloco de biblioteca, a menos que o elemento ao qual eles são aplicados seja referenciado dentro do bloco de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f33d3-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="f33d3-113">As instruções dentro do bloco de biblioteca podem fazer referência a um elemento externo usando-o como um tipo base, herdando dele ou referenciando-o em uma linha, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="f33d3-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="f33d3-114">Se um elemento definido fora do bloco de biblioteca for referenciado dentro do bloco de biblioteca, sua definição será colocada na biblioteca de tipos gerada.</span><span class="sxs-lookup"><span data-stu-id="f33d3-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="f33d3-115">O compilador MIDL trata as instruções fora de um bloco de biblioteca como um arquivo IDL típico e analisa essas instruções, como sempre foi feito.</span><span class="sxs-lookup"><span data-stu-id="f33d3-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="f33d3-116">Normalmente, isso significa gerar stubs de linguagem C para um aplicativo RPC.</span><span class="sxs-lookup"><span data-stu-id="f33d3-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="f33d3-117">Para obter mais informações sobre a sintaxe geral de um arquivo ODL, consulte [sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="f33d3-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 